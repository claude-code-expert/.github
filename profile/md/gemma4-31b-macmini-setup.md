# Gemma 4 on Mac Mini — Ollama 설치 가이드

> **환경**: Mac Mini M4 Pro / 14코어 CPU / 20코어 GPU / 64GB 통합 메모리  
> **도구**: Ollama v0.20.5+

---

## 사전 확인

- Homebrew 설치 필요 (`/opt/homebrew`)
- macOS 최신 버전 권장
- 디스크 여유 공간 25GB 이상

---

## 모델 선택 — 메모리 기준

Mac Mini의 통합 메모리 용량에 따라 권장 모델이 다릅니다.

| 통합 메모리 | 권장 모델 | 다운로드 크기 | 메모리 사용 |
|------------|---------|------------|-----------|
| 16GB | `gemma4:e4b` | ~9.6GB | ~6GB |
| 24GB ~ 47GB | `gemma4:26b` | ~17GB | ~18GB |
| **48GB 이상** | **`gemma4:31b`** | **~19GB** | **~20GB** |

> macOS 시스템이 약 3~5GB를 상시 점유하므로 **48GB 미만이라면 31B 대신 26B를 강력 권장**합니다.  
> 26B MoE 모델은 추론 시 실제 활성 파라미터가 ~4B에 불과해 속도도 31B보다 빠릅니다.

### 48GB 미만 — gemma4:26b

```bash
ollama pull gemma4:26b
```

### 48GB 이상 — gemma4:31b (본 가이드 기준)

```bash
ollama pull gemma4:31b
```

---

## Step 1. Ollama 설치

```bash
brew install --cask ollama-app
```

설치 결과:
- `Ollama.app` → `/Applications/Ollama.app`
- CLI → `/opt/homebrew/bin/ollama`

---

## Step 2. Ollama 실행

```bash
open -a Ollama
```

메뉴바에 Ollama 아이콘이 표시되면 서버 준비 완료.

```bash
# 실행 확인
ollama list
```

---

## Step 3. 모델 다운로드

메모리에 맞는 모델을 선택해서 다운로드하세요.

```bash
# 48GB 미만 Mac Mini → 26B 권장
ollama pull gemma4:26b

# 48GB 이상 Mac Mini → 31B 권장
ollama pull gemma4:31b
```

**31B 기준:**
- 다운로드 크기: **~19GB**
- 로딩 메모리: **~20GB** (Q4_K_M 양자화)
- 64GB 기준 여유 메모리: **~44GB**

**26B 기준:**
- 다운로드 크기: **~17GB**
- 로딩 메모리: **~18GB** (MoE, 활성 파라미터 ~4B)
- 24GB 기준 여유 메모리: **~6GB** (시스템 점유 포함 시 빠듯)

---

## Step 4. 환경변수 설정 (GPU 최적화 + 상시 로딩)

```bash
# 현재 세션에 즉시 적용
launchctl setenv OLLAMA_NUM_GPU 99
launchctl setenv OLLAMA_KEEP_ALIVE "-1"
```

```bash
# 재부팅 후에도 유지 (zshrc 영구 등록)
echo 'export OLLAMA_NUM_GPU=99' >> ~/.zshrc
echo 'export OLLAMA_KEEP_ALIVE="-1"' >> ~/.zshrc
```

> **⚠️ 주의**: 환경변수 적용 후 Ollama를 **반드시 재시작**해야 합니다.

```bash
pkill -x Ollama
sleep 2
open -a Ollama
sleep 3
```

| 환경변수 | 설명 |
|---------|------|
| `OLLAMA_NUM_GPU 99` | 가능한 모든 레이어를 GPU에 올림. 미설정 시 CPU fallback으로 속도 반토막 |
| `OLLAMA_KEEP_ALIVE -1` | 모델 영구 메모리 유지. 기본값은 5분 후 자동 언로드 |

---

## Step 5. 테스트

### 기본 테스트 (단순 실행)

```bash
ollama run gemma4:31b "안녕, 넌 어떤 모델이야?"
```

### 대화형 모드 (컨텍스트 길이 설정 포함)

```bash
ollama run gemma4:31b
```

진입 후:

```
>>> /set parameter num_ctx 32768
Set parameter 'num_ctx' to '32768'

>>> 안녕, 넌 어떤 모델이야?
```

> **⚠️ 주의**: `--num-ctx` 플래그는 대화형 모드에서만 동작합니다.  
> `ollama run gemma4:31b --num-ctx 32768 "..."` 형태는 지원하지 않습니다.

### 권장 컨텍스트 길이

| 컨텍스트 | 추가 메모리 | 추천 용도 |
|---------|-----------|---------|
| 8,192 | ~0.6GB | 빠른 테스트, 짧은 대화 |
| 32,768 | ~2.5GB | **일반 사용 권장** |
| 65,536 | ~5GB | 긴 문서 분석 |
| 131,072 | ~10GB | 코드베이스 전체 컨텍스트 |

---

## Step 6. 상태 확인

```bash
ollama ps
```

정상 출력 예시:

```
NAME           SIZE    PROCESSOR        CONTEXT    UNTIL
gemma4:31b     20 GB   12%/88% CPU/GPU  32768      Forever
```

- `CPU/GPU` 비율에서 GPU 비중이 높을수록 정상
- `UNTIL` 컬럼이 `Forever`이면 Keep-alive 정상 적용

---

## Step 7. 자동 시작 설정 (선택)

### 7a. 로그인 시 Ollama 자동 실행

메뉴바 아이콘 → **Launch at Login** 체크  
또는: **시스템 설정 > 일반 > 로그인 항목**에서 Ollama 추가

### 7b. 부팅 시 모델 자동 프리로드 (LaunchAgent)

> **⚠️ 주의**: `~/Library/LaunchAgents/` 폴더가 없으면 `permission denied` 오류가 발생합니다.  
> 아래 명령어에 `mkdir -p`가 포함되어 있으니 **그대로** 실행하세요.  
> 또한 plist 내부 DOCTYPE 라인에 백슬래시(`\`)가 섞이지 않도록 주의하세요 (복사 시 오염 주의).

```bash
# LaunchAgents 폴더 생성 (없을 경우 대비)
mkdir -p ~/Library/LaunchAgents

cat << 'EOF' > ~/Library/LaunchAgents/com.ollama.preload-gemma4.plist
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>Label</key>
    <string>com.ollama.preload-gemma4</string>
    <key>ProgramArguments</key>
    <array>
        <string>/opt/homebrew/bin/ollama</string>
        <string>run</string>
        <string>gemma4:31b</string>
        <string></string>
    </array>
    <key>RunAtLoad</key>
    <true/>
    <key>StartInterval</key>
    <integer>300</integer>
    <key>StandardOutPath</key>
    <string>/tmp/ollama-preload.log</string>
    <key>StandardErrorPath</key>
    <string>/tmp/ollama-preload.log</string>
</dict>
</plist>
EOF

launchctl load ~/Library/LaunchAgents/com.ollama.preload-gemma4.plist
echo "완료: $?"
```

마지막 줄에 `완료: 0` 이 출력되면 성공입니다.

---

## API 연동 (OpenAI 호환)

```bash
curl http://localhost:11434/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gemma4:31b",
    "messages": [{"role": "user", "content": "안녕"}]
  }'
```

기존 OpenAI SDK 코드에서 base URL만 변경하면 그대로 사용 가능:

```python
from openai import OpenAI

client = OpenAI(
    base_url="http://localhost:11434/v1",
    api_key="ollama"  # 아무 값이나 가능
)

response = client.chat.completions.create(
    model="gemma4:31b",
    messages=[{"role": "user", "content": "안녕"}]
)
print(response.choices[0].message.content)
```

---

## 유용한 명령어 모음

| 명령어 | 설명 |
|--------|------|
| `ollama list` | 다운로드된 모델 목록 |
| `ollama ps` | 현재 로딩된 모델 및 메모리 |
| `ollama run gemma4:31b` | 대화형 모드 진입 |
| `ollama stop gemma4:31b` | 메모리에서 모델 언로드 |
| `ollama pull gemma4:31b` | 최신 버전으로 업데이트 |
| `ollama rm gemma4:31b` | 모델 삭제 |

---

## 제거 방법

```bash
# LaunchAgent 제거
launchctl unload ~/Library/LaunchAgents/com.ollama.preload-gemma4.plist
rm ~/Library/LaunchAgents/com.ollama.preload-gemma4.plist

# Ollama 제거
brew uninstall --cask ollama-app
```

---

## 트러블슈팅

| 증상 | 원인 | 해결 |
|------|------|------|
| `Error: unknown flag: --num-ctx` | 인라인 명령어에서 플래그 불가 | 대화형 모드 진입 후 `/set parameter num_ctx 값` 사용 |
| 응답 없음 (첫 실행) | 20GB 모델 로딩 중 | 30~60초 대기, `ollama ps`로 확인 |
| GPU 비중 낮음 (CPU 80%+) | 환경변수 미적용 | Ollama 재시작 후 `OLLAMA_NUM_GPU 99` 재설정 |
| 메모리 부족 오류 | 컨텍스트 너무 큼 | `num_ctx` 값을 8192로 낮춰서 재시도 |
| 느린 속도 (1 tok/s 미만) | CPU fallback | `ollama ps`에서 GPU 비중 확인, Ollama 재시작 |
| `permission denied: .../com.ollama.preload-gemma4.plist` | `~/Library/LaunchAgents` 폴더 없음 | `mkdir -p ~/Library/LaunchAgents` 실행 후 재시도 |
| `Load failed: 5: Input/output error` | plist 문법 오류 (백슬래시 오염 등) | plist 파일 삭제 후 Step 7b 명령어를 처음부터 다시 실행 |
