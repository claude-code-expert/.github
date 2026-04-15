<div align="center">

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/banner.png" alt="Claude Code Expert" width="100%" />


<br/>

**AI와 함께하는 개발 — 원칙, 방법론, 그리고 실전 코드**

[![Book](https://img.shields.io/badge/Book-Claude_Code_Master-2E75B6?style=for-the-badge&logo=bookstack&logoColor=white)](#소개)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

[English](https://github.com/claude-code-expert/.github/blob/main/profile/README.en.md) · **한국어**

</div>

---

### 소개

<table>
<tr>
<td width="35%" align="center" valign="top">

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/cc-master.png" alt="클로드 코드 마스터" width="100%" />

<br/>

<a href="https://product.kyobobook.co.kr/detail/S000219725328" target="_blank"><img src="https://img.shields.io/badge/클로드_코드_마스터-온라인_구매-2E75B6?style=for-the-badge&logo=bookstack&logoColor=white" alt="클로드 코드 마스터 온라인 구매" /></a>

</td>
<td width="65%" valign="top">

**Claude Code Expert**는 『클로드 코드 마스터 — 기획 · 개발 · 운영이 한 번에 끝나는 AI 에이전틱 코딩 워크 플로』의 공식 GitHub 조직입니다.

이 책은 단순한 도구 사용법 튜토리얼이 아닙니다. AI 코딩 에이전트와 체계적으로 협업하는 방법론을 제시합니다 — 명세 주도 개발(SDD), 테스트 주도 개발(TDD), 그리고 어떤 AI 도구를 사용하든 변하지 않는 체계적인 리뷰 프로세스까지 다룹니다.

책에 수록된 모든 예제 코드, 프로젝트 템플릿과 예제, 참고 자료가 이 레파지터리에서 관리됩니다.

#### 이 조직에서 제공하는 것

이 조직은 책의 companion 레포지토리와 함께, 클로드 코드로 직접 개발한 오픈소스 사이드 프로젝트를 호스팅합니다. 각 레포지토리는 책에서 논의하는 원칙과 워크플로우를 통해 개발한 완성 코드를 보여주며, 티켓 기반 칸반 보드, 챗봇 개발 프로젝트의 명세 작성부터 개발 방법, 배포까지 예제 코드와 함께 단계별로 완성해 나갑니다.

책 분량상 포함하지 못한 Subagent 개발, 마크다운 기반 지식 저장소, 홈서버 호스팅을 쉽게 구축하는 Brewnet, 각 프레임워크의 보일러 플레이트 16종 등이 2026년 출판 시점 기준으로 완성되어 있습니다.

책 관련 문의 사항이나 프로젝트 관련 문의사항은 brewnet.dev@gmail.com으로 연락주시기 바랍니다.

</td>
</tr>
</table>

---

### 📦 레포지토리

#### 책 예제 프로젝트

#### [example](https://github.com/claude-code-expert/example) — 문서화 가이드 & 템플릿 모음

책에 수록된 프로젝트 문서 템플릿과 Claude Code 설정 예제 모음입니다. 클로드 코드 개발에 필요한 필수 문서 체계(PRD, TRD, REQUIREMENTS), CLAUDE.md/AGENTS.md 템플릿, 스킬, 훅, 규칙, CLI 치트시트를 제공합니다.

- **주요 내용**: 문서 템플릿 · 코딩 컨벤션 · 스킬 & 훅 예제 · Claude Code 치트시트 · 프롬프트 엔지니어링 · 컨텍스트 엔지니어링 · 하네스 엔지니어링 및 서브에이전트에 대한 설명과 가이드 문서들을 제공

## Skills (3개)

커스텀 AI 워크플로우 정의 파일 (`skills/`)

| 스킬 | 설명 |
|------|------|
| `test-driven-development.md` | RED-GREEN-REFACTOR TDD 워크플로우 |
| `code-reviewer.md` | PR 및 코드 품질 리뷰 (읽기 전용) |
| `react-component.md` | 팀 컨벤션 기반 React 컴포넌트 생성 |

## Commands (2개)

커스텀 슬래시 명령어 (`.claude/commands/`)

| 명령어 | 설명 |
|--------|------|
| `/optimize` | 코드베이스 문서 분석 후 실행 명령어 제안 |
| `/security-checklist` | 7개 카테고리 보안 점검 (입력 검증, SQL 인젝션, XSS, 환경변수, 의존성, API, 권한) |

## Hooks (12개)

자동화 스크립트 (`.claude/hooks/`)

| 카테고리 | 파일 | 트리거 |
|----------|------|--------|
| **보안 차단** | `block-dangerous.py` | PreToolUse — `rm -rf`, `force push`, `DROP TABLE` 등 차단 |
| **의존성 검사** | `check-deps-py.py` | PreToolUse — Python import 누락 경고 |
| **포맷팅** | `format-ts.sh`, `format-py.sh` | PostToolUse — 저장 시 자동 포맷 |
| **린팅** | `lint-ts.sh`, `lint-py.sh` | PostToolUse — 수정 시 린트 실행 |
| **테스트** | `test-ts.sh`, `test-py.sh` | PostToolUse — 자동 테스트 실행 |
| **알림** | `notify-slack.sh` | Notification/Stop — Slack 웹훅 알림 |
| **알림** | `notify-telegram.sh` | Notification/Stop — Telegram 봇 알림 |
| **설정** | `settings.typescript.json`, `settings.python.json` | 언어별 훅 설정 오버라이드 |

## Rules (4개)

경로 기반 코딩 규칙 (`.claude/rules/`)

| 규칙 | 적용 경로 | 핵심 내용 |
|------|-----------|-----------|
| `api-routes.md` | `src/api/**/*.ts` | 응답 형식, 에러 처리, 인증, Zod 검증 |
| `frontend.md` | `src/components/**/*.tsx` | 함수형 컴포넌트, Tailwind, 접근성 |
| `testing.md` | `**/*.test.ts` | AAA 패턴, describe/it 네이밍, Mock 관리 |
| `database.md` | `src/models/**/*.ts` | 모델 정의, N+1 방지, 페이지네이션, 인덱스 |

## 템플릿 (17개)

재사용 가능한 설정 템플릿 (`template/`)

| 분류 | 파일 | 설명 |
|------|------|------|
| **CLAUDE.md** | `CLAUDE.md` | 전체 예제 |
| | `CLAUDE.local.md` | 개인 설정 (gitignore 대상) |
| | `CLAUDE-template(Root).md` | 모노레포 루트용 |
| | `CLAUDE-template(Client).md` | 클라이언트용 |
| | `CLAUDE-template(Server).md` | 서버용 |
| **AGENTS.md** | `AGENTS-Guide.md` | 작성 가이드 |
| | `AGENTS-template.md` | 기본 템플릿 |
| | `AGENTS(java-back).md` | Spring Boot 예제 |
| **컨벤션** | `code-style.md` | 코딩 스타일 (네이밍, 포맷, 타입) |
| | `root-code-style.md` | 모노레포 루트 코드 스타일 |
| | `patterns.md` | 아키텍처 패턴 |
| | `client-patterns.md` | 클라이언트 패턴 (컴포넌트, 훅, 상태) |
| | `server-patterns.md` | 서버 패턴 (미들웨어, 검증, 에러) |
| | `git-workflow.md` | Git 브랜치 전략, 커밋, PR |
| | `testing.md` | 테스트 전략 (단위, 통합, E2E) |
| **기타** | `skill-template.md` | 스킬 작성 템플릿 |
| | `settings.json` | settings.json 주석 포함 예제 |

## 프로젝트 문서 (7개)

3계층 문서 체계 + 외부 도구 가이드 (`docs/`)

| 계층 | 파일 | 설명 |
|------|------|------|
| 비즈니스 | `PRD.md` | 제품 요구사항 정의서 |
| 아키텍처 | `TRD.md` | 기술 요구사항 정의서 |
| 구현 | `REQUIREMENTS.md` | AI 구현 요구사항 |
| 레퍼런스 | `COMMANDS.md` | 슬래시 명령어 전체 정리 |
| 외부 도구 | `SpecKit_Guide.md` | Spec-Driven Development 프레임워크 |
| | `SuperClaude_Guide.md` | Claude Code 전용 확장 (30+ 명령어) |
| | `Vercel_Agent_Skills_Guide.md` | 17+ AI 에이전트 호환 스킬 생태계 |

## 엔지니어링 가이드 (4개)

심화 학습 자료 (`guide/`)

| 가이드 | 핵심 내용 |
|--------|-----------|
| `prompt-engineering-guide.md` | 제로샷, 퓨샷, CoT 등 프롬프팅 기법 |
| `context-engineering-guide.md` | AI가 보는 전체 맥락 설계 방법 |
| `harness-engineering-guide.md` | 에이전트 품질 보증 구조 (Hooks, Rules, 자동 검증) |
| `claude-code-hooks-guide.md` | Hooks 시스템 상세 (타이밍, 환경변수, 매처) |

## 레퍼런스 (4개)

치트시트 & CLI 명령어

| 문서 | 설명 |
|------|------|
| `claude-code-cheatsheet-ko` | v2.1.91 단축키, 명령어, 설정, MCP, 권한 (HTML/MD) |
| `claude-code-unshipped` | npm 소스 기반 23개 미출시 기능 분석 (HTML/MD) |
| `git_cli.md` | Git 필수/고급 명령어 모음 |
| `postgres_cli.md` | PostgreSQL 접속, 관리, CRUD, 백업 명령어 |

## 실전 팁 (3개)

Claude Code 활용 꿀팁 (`tips/`)

| 문서 | 설명 |
|------|------|
| `CLAUDE-CODE-CLI-ALIAS-SETTINGS.md` | CLI 플래그 65+개, 셸 별칭 20+개, 위험 모드 가이드 |
| `CLAUDE-CODE-NTFY-MOBILE-APPROVAL.md` | ntfy 모바일 승인 알림 설정 |
| `lsp.md` | LSP 연동 3가지 방법 비교 (공식 플러그인, cclsp, Serena) |

## 서브에이전트 가이드

| 문서 | 설명 |
|------|------|
| `subagent/subagent.md` | 서브에이전트 개념, 동작 원리, 정의 형식, 우선순위, Agent Teams 비교 |

#### [tika](https://github.com/claude-code-expert/tika) — 티켓 기반 칸반 보드 TODO 앱 (Part 2)

책의 Part 2 전체에서 사용하는 핵심 예제 프로젝트입니다. Claude Code를 활용하여 SDD와 TDD 방법론으로 개발한 풀스택 칸반 보드 애플리케이션으로 예제 이후의 확장과 SaaS 서비스 개발을 목표로 개발했습니다.

---

## 기술 스택

| 영역 | 기술 |
|---|---|
| **프레임워크** | Next.js 15 (App Router) |
| **언어** | TypeScript |
| **스타일링** | Tailwind CSS 4 |
| **ORM / DB** | Drizzle ORM · Vercel Postgres (Neon) |
| **인증** | NextAuth.js v5 (Google OAuth) |
| **배포** | Vercel |

---

## 개발 방법론

SDD(Specification-Driven Development) 전체 워크플로우 적용

```
PRD → TRD → REQUIREMENTS.md → API 명세 → 컴포넌트 명세 → 테스트 케이스 → 구현
```

---

## 핵심 기능

### 칸반 보드

- **4단계 고정 칼럼**: Backlog → TODO → In Progress → Done
- **드래그 앤 드롭**: 칼럼 간 이동 및 칼럼 내 순서 변경
- **우선순위 4단계**: LOW · MEDIUM · HIGH · CRITICAL
- **마감일 관리**: 오버듀 시 시각적 경고 표시
- **휴지통**: 삭제 티켓 복원 가능 (Soft Delete)

### 티켓 관리

- **CRUD**: 생성 · 조회 · 수정 · 삭제
- **이슈 계층 구조**: Goal → Story → Feature → Task 4단계 분해
- **체크리스트**: 하위 작업 목록 (티켓당 최대 20개)
- **라벨/태그**: 6개 프리셋 + 커스텀 라벨 (티켓당 최대 5개)
- **담당자 배정**: 멤버 기반 할당

### 팀 워크스페이스

- **멤버 관리**: OWNER · ADMIN · MEMBER · VIEWER 역할 구분
- **초대 시스템**: 링크 기반 팀 초대
- **스프린트**: 스프린트 단위 작업 계획
- **WBS (Work Breakdown Structure)**: 이슈 계층 시각화
- **간트 차트**: 일정 및 진행 현황 타임라인

### 분석 대시보드

| 차트 | 설명 |
|---|---|
| **번다운 차트** | 스프린트별 잔여 작업량 추이 |
| **누적 흐름 다이어그램 (CFD)** | 상태별 티켓 누적 현황 |
| **벨로시티 차트** | 스프린트 처리 속도 분석 |
| **사이클 타임 분석** | 티켓 완료까지 소요 시간 |
| **우선순위-상태 매트릭스** | 우선순위 × 상태 분포 |
| **라벨 분석** | 라벨별 티켓 분포 |
| **워크로드 히트맵** | 멤버별 작업 부하 시각화 |
| **트렌드 차트** | 기간별 생성·완료 티켓 추이 |

### 알림 시스템

- **마감일 D-1 알림**: Vercel Cron으로 자동 발송
- **Slack 연동**: Incoming Webhook 기반 채널 알림
- **Telegram 연동**: Bot API 기반 메시지 알림
- **심각도별 라우팅**: P0·P1(Slack+Telegram) / P2(Slack) / P3(로그)
- **알림 내역**: 읽음/안 읽음 상태 관리

### 기타

- **Google OAuth**: NextAuth.js v5 기반 소셜 로그인
- **워크스페이스 전환**: 개인·팀 워크스페이스 멀티 관리
- **반응형 디자인**: 모바일(360px) ~ 데스크톱(1920px)
- **다중 워크스페이스**: 개인 플랜, 팀 플랜 및 설치형 서비스 무료로 사용 가능(오픈소스)


<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika_intro.png" alt="Tika 소개" width="100%" />
<p align="center"><em>Tika Intro</em></p>

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika_main.png" alt="Tika 칸반 보드 메인" width="100%" />
<p align="center"><em>Tika Main</em></p>

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika_board.png" alt="Tika 칸반 대시보드" width="100%" />
<p align="center"><em>Tika Kanban board</em></p>

---

## 기술 스택

| 영역 | 기술 |
|---|---|
| **프레임워크** | Next.js 15 (App Router) |
| **언어** | TypeScript |
| **스타일링** | Tailwind CSS 4 |
| **ORM / DB** | Drizzle ORM · Vercel Postgres (Neon) |
| **인증** | NextAuth.js v5 (Google OAuth) |

- **주요 기능**: 드래그 앤 드롭 칸반 보드, 티켓 CRUD, 상태 관리, 우선순위 정렬
- **개발 방법론**: SDD 전체 워크플로우 — PRD → TRD → REQUIREMENTS.md → API 명세 → 컴포넌트 명세 → 테스트 케이스 → 구현
- **웹사이트**: [tika-app.vercel.app](https://tika-app.vercel.app/login)

#### [todo-app](https://github.com/claude-code-expert/todo-app) — 칸반 보드 TODO 앱 (6장)

클로드 코드 마스터 파트 2의 실습 칸반 보드 앱입니다. Tika의 프로토타입으로 단일 사용자 환경에서 4개 칼럼(Backlog, TODO, In Progress, Done)으로 티켓을 관리하며, 드래그앤드롭을 지원합니다. 

- **기술 스택**: Next.js 15 · React 19 · TypeScript · Tailwind CSS 4 · Drizzle ORM · @dnd-kit
- **주요 기능**: 티켓 CRUD, 드래그앤드롭 재정렬, 오버듀 감지, 필터 바
- **데모**: [ticket-kanban.vercel.app](https://ticket-kanban.vercel.app)

#### [chatbot](https://github.com/claude-code-expert/chatbot) — AWS Bedrock AI 챗봇 (Part 3)

Part 3(중급편)의 웹 기반 AI 챗봇 애플리케이션입니다. SSE를 통한 실시간 스트리밍 응답과 Tool Use를 지원하며 AWS Bedrock Claude 모델을 활용합니다.

- **기술 스택**: React 19 · Vite · Express 5 · TypeScript · Tailwind CSS · shadcn/ui · AWS Bedrock
- **주요 기능**: SSE 토큰 스트리밍, Tool Use (계산기, 시간, 날씨), 다중 세션 관리, 다크/라이트 테마, Markdown 렌더링

#### [subagents](https://github.com/claude-code-expert/subagents) — Squad Agent 시스템

Claude Code 서브에이전트 시스템으로, 자동화된 개발 워크플로우를 위한 8개 전문 에이전트를 제공합니다. 원라인 설치, 파이프라인 기반 체이닝, OS 네이티브 알림을 지원합니다.

- **에이전트**: review · plan · refactor · qa · debug · docs · gitops · audit
- **주요 특징**: 모델 라우팅 (Opus/Sonnet/Haiku), 파이프라인 체이닝, SubagentStart/Stop 훅, 크로스플랫폼 알림
- **설치**: `curl -sL https://raw.githubusercontent.com/claude-code-expert/subagents/main/install.sh | bash`

#### 오픈소스 사이드 프로젝트

#### [brewnet](https://github.com/claude-code-expert/brewnet) — 셀프호스팅 홈 서버 자동 구축 도구

단 하나의 명령어로 완전한 셀프호스팅 홈 서버를 구축하는 오픈소스 CLI 도구입니다. 실전 사이드 프로젝트로서 전체가 Claude Code로 개발되었습니다.

#### 왜 사용하는가?
  복잡한 서버 지식 없이 명령어 한 줄(brewnet init)로 완전한 셀프호스팅 홈 서버를 구축. 포트포워딩 없이 Cloudflare Tunnel로 외부 접속까지 자동화.                      
<br>                                                                                                                                                                      
  핵심 특징                                                                                                                                                           
  - 8단계 대화형 위저드 — Git 서버 · DB · 파일 서버 · 미디어 서버 한번에 구성
  - Docker 미설치 상태에서도 자동 설치 후 진행 (macOS + Linux)
  - 16개 스택 앱 스캐폴딩 (brewnet create-app) — Gitea 저장소 + Traefik 라우팅 포함 
  - 웹 어드민 대시보드(localhost:8088) — 실시간 로그 · 배포 히스토리 · 도메인 연결 관리 
  - 백업 · 복원 · 언인스톨까지 CLI 단일 도구로 완전 제어
  - 설치 부터 도메인 연결까지 3분(네트워크 환경에 따라 다소 차이가 날 수 있습니다) 내외의 초고속 셀프호스팅 홈서버 구축 
  - 홈페이지성 정적 컨텐츠 다이렉트 호스팅(github, cloudflare 직접 연결 및 내부 호스팅 가능) 


<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/brewnet-web.png" alt="Brewnet 웹사이트" width="100%" />

- **기술 스택**: TypeScript 5 · Node.js 20 · Docker Compose · Traefik · Cloudflare Tunnel · Commander.js · SQLite  
- **주요 기능**: 7단계 대화형 위저드, Docker 자동 설치, Git/DB/파일/미디어 서버 구성, Cloudflare Tunnel 외부 접속
- **웹사이트**: [www.brewnet.dev](https://www.brewnet.dev)

#### [brewnet-boilerplate](https://github.com/claude-code-expert/brewnet-boilerplate) — 풀스택 보일러플레이트 모음

Brewnet의 공식 보일러플레이트 모노레포로, 6개 프로그래밍 언어에 걸쳐 16개의 프로덕션 레디 풀스택 템플릿을 제공합니다. 단일 명령어로 실행 가능합니다.

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/brewnet-boilerplate.png" alt="Brewnet 보일러플레이트" width="100%" />

- **지원 언어**: Go · Rust · Java · Kotlin · Node.js · Python
- **지원 프레임워크 보일러플레이트**: Gin, Echo, Fiber, Actix-web, Axum, Spring Boot, Spring, Ktor, Express, NestJS, Next.js, FastAPI, Django, Flask
- **주요 특징**: 전 스택 통일된 API 규약, 멀티 데이터베이스 지원 (PostgreSQL/MySQL/SQLite3), Docker 멀티스테이지 빌드, 관리 대시보드


#### 스타터 템플릿

#### [nodejs](https://github.com/claude-code-expert/nodejs) — 미니멀 Node.js 웹 앱

Railway에 원클릭 배포 가능한 미니멀 Node.js 웹 애플리케이션 스타터입니다.

- **기술 스택**: Node.js
- **배포**: [Railway](https://railway.app)

#### [java-spring-boot](https://github.com/claude-code-expert/java-spring-boot) — Spring Boot 스타터 앱

Railway에 원클릭 배포 가능한 Spring Boot 스타터 애플리케이션입니다.

- **기술 스택**: Java · Spring Boot
- **배포**: [Railway](https://railway.app)

---

### 👥 저자

<table>
<tr>
<td width="50%" valign="top">

#### 이남희 (Namhee Lee)

**카카오 서버 개발자**

20년 경력의 소프트웨어 엔지니어로, 업계의 다양한 분야를 두루 경험했다. 제약회사 전산실에서 첫 직장생활을 시작하여 WAS 기술 벤더를 거쳐, 커머스·통신·전자 등 대규모 SI 프로젝트에서 서비스 도메인 개발을 맡으며 공통 프레임워크 개발 담당 및 애플리케이션 아키텍트로 활약했다.

2012년 스터디 그룹에서 만든 오픈소스 프로덕트로 공개 SW 개발자 대회에 입상한 후, **쿠팡**에 입사하여 4년간 주문/배송 시스템의 MSA 분리 개발과 여행 예약 서비스 개발을 수행했다. 이후 LF를 거쳐 카카오에서 셀장, 파트장, 리더를 역임했으나, AI 코딩 도구의 잠재력을 목격한 후 실무로 복귀하여 현재는 서버 개발자로 근무하고 있다.

2024년에는 <a href="https://www.hanbit.co.kr/media/" target="_blank">한빛미디어</a>를 통해 개발자 기술면접 노트(https://product.kyobobook.co.kr/detail/S000216231695) 라는 책을 출간했으며, 현재는 사이드 프로젝트로 노트앱 (https://www.q-note.app)과 홈서버 자동 구축 솔루션인 브루넷(https://www.brewnet.dev) 등 다양한 아이디어를 AI 도구를 통해 구현하는데 재미를 느끼고 있다. 

[![GitHub](https://img.shields.io/badge/GitHub-villainscode-181717?logo=github)](https://github.com/villainscode)
[![Email](https://img.shields.io/badge/Email-villainscode@gmail.com-EA4335?logo=gmail&logoColor=white)](mailto:villainscode@gmail.com)

</td>
<td width="50%" valign="top">

#### 백승현 (Seunghyun Baek)

**디스패치(Dispatch) CTO**

2002년 개발자로 커리어를 시작해 한국과 일본을 오가며 20년 이상 소프트웨어 개발 경험을 쌓았다. 일본에서 닛산자동차 웹사이트 빌드 툴, 미즈호은행 대출시스템, 상공중금 영업지원시스템 등 대규모 금융·제조 프로젝트에 리더로 참여하며 시스템 설계와 팀 리딩 경험을 쌓았다. 이후 한국으로 돌아와 YES24의 전자책 리더기 **크레마** 초기 버전 개발에 참여했다.

2014년부터 한국 최대 연예 미디어 **디스패치**의 CTO로 재직 중이다. 한국 미디어 기업 최초로 AWS 클라우드 도입을 주도했으며, 자체 CMS, 광고관리시스템, 포토/비디오 DB 등 핵심 시스템을 직접 설계·구축했다. 수천만 명이 동시 접속하는 특종 보도 상황에서도 안정적인 서비스 운영 체계를 구축하여 트래픽 대응 비용을 70% 절감했으며, 대규모 웹 트래픽 분석 툴을 개발해 데이터 기반의 미디어 운영 전략을 지원하고 있다. 2013년 공개 SW 개발자 대회 금상 수상.


[![Email](https://img.shields.io/badge/Email-pekuid@gmail.com-EA4335?logo=gmail&logoColor=white)](mailto:pekuid@gmail.com)

</td>
</tr>
</table>

---

### 📖 책 구성

이 책은 이론에서 실전으로, 기초에서 심화로 자연스럽게 이어지는 네 개의 파트로 구성되어 있습니다.

| 파트 | 제목 | 내용 |
|:----:|------|------|
| **1** | 시작하기 전에 | 개발자 패러다임 전환, Claude Code 설정, AI 협업 방법론 (TDD, SDD, MCP) |
| **2** | 기초편 | 풀스택 TODO 앱 (Tika) — 요건 정의 → 설계 → 개발 → 테스트 → 배포 |
| **3** | 중급편 | AWS Bedrock 기반 AI 챗봇 — 스트리밍, 컨텍스트 관리, Tool Use, 고급 활용 기법, 할루시네이션 대응 |


**핵심 철학**: *도구는 바뀌어도 원칙은 변하지 않는다.* 이 책의 방법론은 Claude Code, Cursor, Copilot, Codex, 그 어떤 AI 코딩 에이전트에도 그대로 적용할 수 있습니다.

---

### 📬 연락처

책 또는 이 조직에 대한 문의는 저자 이메일 또는 GitHub를 통해 연락해 주세요.

---

<div align="center">
 독자와 함께 가꿔나가는 공간입니다. Star나 Fork로 작은 응원을 보내주길 부탁드립니다.
</div>
