# GitHub Organization Setup Guide
# claude-code-expert 조직 설정 가이드

---

## 1. Organization Description (조직 설명)

GitHub 조직 Settings → Profile에 입력할 내용입니다.

### Description (160자 제한)
```
Official code repository for "Claude Code Expert" — AI-assisted development from design to deployment. 설계부터 배포까지, AI와 함께하는 개발.
```

### URL
```
https://github.com/claude-code-expert
```

---

## 2. Profile README 설정 방법

GitHub 조직 프로필 README를 적용하려면 다음 단계를 따르세요:

### Step 1: `.github` 레포지토리 생성
조직 내에 `.github`이라는 이름의 **public** 레포지토리를 생성합니다.

### Step 2: profile 디렉토리 생성
`.github` 레포지토리 안에 `profile/` 디렉토리를 만듭니다.

### Step 3: README.md 배치
첨부된 `profile-README.md` 파일의 내용을 `.github/profile/README.md`로 저장합니다.

### 최종 구조
```
claude-code-expert/.github/
├── profile/
│   ├── README.md              ← 조직 프로필 페이지에 표시
│   └── assets/
│       ├── banner.png         ← 상단 배너 이미지 (1280x420)
│       └── tika-screenshot.png ← Tika 앱 스크린샷
```

---

## 3. 이미지 파일 배치

### 조직 아바타 (프로필 사진)
- GitHub 조직 Settings → Profile → Upload new picture
- 첨부된 `avatar-logo.png` (800x800) 또는 `avatar-simple.png` (400x400) 사용
- 800x800 버전은 텍스트 포함, 400x400 버전은 심볼 중심

### 배너 이미지
- `.github/profile/assets/` 디렉토리에 `banner.png` 업로드
- README.md에서 자동으로 참조됨

### Tika 스크린샷 캡처 방법
1. https://tika-kappa.vercel.app 접속
2. 브라우저 전체 너비로 캡처 (권장: 1280px 이상)
3. `.github/profile/assets/tika-screenshot.png`로 저장
4. 파일명이 다르면 README.md의 이미지 경로도 함께 수정

---

## 4. 레포지토리별 Description 설정

각 레포지토리의 Settings → About에 입력할 Description입니다.

### tika
```
Ticket-based Kanban Board TODO App — Book example project built with SDD/TDD methodology using Claude Code
```

### brewnet
```
Self-hosted stack bootstrapper · Docker Compose · Git server · File manager · One command setup
```
*(이미 설정되어 있음)*

### brewnet-boilerplate
```
16 production-ready full-stack boilerplates across 6 languages · One command app creation
```

---

## 5. 추후 추가 예정 레포지토리

책의 내용에 따라 다음 레포지토리가 추가될 수 있습니다:

| 레포지토리 | 용도 | 책 파트 |
|-----------|------|--------|
| `chatbot` | AI 챗봇 애플리케이션 예제 | Part 3 (중급편) |
| `example` | Markdown 문서 템플릿, CLAUDE.md 예시 등 | 부록 |

