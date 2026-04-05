<div align="center">

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/banner.png" alt="Claude Code Expert" width="100%" />


<br/>

**AI와 함께하는 개발 — 원칙, 방법론, 그리고 실전 코드**

[![Book](https://img.shields.io/badge/Book-Claude_Code_Expert-2E75B6?style=for-the-badge&logo=bookstack&logoColor=white)](#소개)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

[English](https://github.com/claude-code-expert/.github/blob/main/profile/README.md) · **한국어**

</div>

---

### 소개

**Claude Code Expert**는 『Claude Code Expert — 설계부터 배포까지, AI와 함께하는 개발』의 공식 GitHub 조직입니다.

이 책은 단순한 도구 사용법 튜토리얼이 아닙니다. AI 코딩 에이전트와 체계적으로 협업하는 방법론을 제시합니다 — 명세 주도 개발(SDD), 테스트 주도 개발(TDD), 그리고 어떤 AI 도구를 사용하든 변하지 않는 체계적인 리뷰 프로세스까지 다룹니다.

책에 수록된 모든 예제 코드, 프로젝트 템플릿, 참고 자료가 이 조직에서 관리됩니다.

### 이 조직에서 제공하는 것

이 조직은 책의 companion 레포지토리와 함께, Claude Code로 직접 개발한 오픈소스 사이드 프로젝트를 호스팅합니다. 각 레포지토리는 책에서 논의하는 원칙과 워크플로우를 실제로 보여줍니다 — 명세 작성부터 배포까지.

---

### 📦 레포지토리

#### 책 예제 프로젝트

#### [example](https://github.com/claude-code-expert/example) — 문서화 가이드 & 템플릿 모음

책에 수록된 프로젝트 문서 템플릿과 Claude Code 설정 예제 모음입니다. 3계층 문서 체계(PRD → TRD → REQUIREMENTS), CLAUDE.md/AGENTS.md 템플릿, 스킬, 훅, 규칙, CLI 치트시트를 제공합니다.

- **주요 내용**: 문서 템플릿 · 코딩 컨벤션 · 스킬 & 훅 예제 · Claude Code 치트시트 · 서브에이전트 가이드
- **특징**: 3계층 문서 구조, 훅 스크립트 12개, 규칙 템플릿 4종, 외부 도구 가이드 (SpecKit, SuperClaude, Vercel Agent Skills)

#### [tika](https://github.com/claude-code-expert/tika) — 티켓 기반 칸반 보드 TODO 앱 (Part 2)

책의 Part 2 전체에서 사용하는 핵심 예제 프로젝트입니다. Claude Code를 활용하여 SDD와 TDD 방법론으로 개발한 풀스택 칸반 보드 애플리케이션입니다.

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika_intro.png" alt="Tika 소개" width="100%" />
<p align="center"><em>Tika Intro</em></p>

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika_main.png" alt="Tika 칸반 보드 메인" width="100%" />
<p align="center"><em>Tika Main</em></p>

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika_board.png" alt="Tika 칸반 대시보드" width="100%" />
<p align="center"><em>Tika Kanban board</em></p>

- **기술 스택**: Next.js 15 (App Router) · TypeScript · Tailwind CSS 4 · Drizzle ORM · Vercel Postgres
- **주요 기능**: 드래그 앤 드롭 칸반 보드, 티켓 CRUD, 상태 관리, 우선순위 정렬
- **개발 방법론**: SDD 전체 워크플로우 — PRD → TRD → REQUIREMENTS.md → API 명세 → 컴포넌트 명세 → 테스트 케이스 → 구현
- **데모**: [tika-app.vercel.app](https://tika-app.vercel.app/login)

#### [todo-app](https://github.com/claude-code-expert/todo-app) — 칸반 보드 TODO 앱 (6장)

6장의 companion 칸반 보드 앱입니다. 단일 사용자 환경에서 4개 칼럼(Backlog, TODO, In Progress, Done)으로 티켓을 관리하며, 드래그앤드롭을 지원합니다. 26개 테스트 스위트, 169개 테스트 통과.

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

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/brewnet-web.png" alt="Brewnet 웹사이트" width="100%" />

- **기술 스택**: TypeScript · Node.js · Docker Compose
- **주요 기능**: 7단계 대화형 위저드, Docker 자동 설치, Git/DB/파일/미디어 서버 구성, Cloudflare Tunnel 외부 접속
- **웹사이트**: [www.brewnet.dev](https://www.brewnet.dev)

#### [brewnet-boilerplate](https://github.com/claude-code-expert/brewnet-boilerplate) — 풀스택 보일러플레이트 모음

Brewnet의 공식 보일러플레이트 모노레포로, 6개 프로그래밍 언어에 걸쳐 16개의 프로덕션 레디 풀스택 템플릿을 제공합니다. 단일 명령어로 실행 가능합니다.

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/brewnet-boilerplate.png" alt="Brewnet 보일러플레이트" width="100%" />

- **지원 언어**: Go · Rust · Java · Kotlin · Node.js · Python
- **프레임워크**: Gin, Echo, Fiber, Actix-web, Axum, Spring Boot, Spring, Ktor, Express, NestJS, Next.js, FastAPI, Django, Flask
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

2024년에는 한빛미디어를 통해 개발자 기술면접 노트(https://product.kyobobook.co.kr/detail/S000216231695)라는 책을 출간했으며, 현재는 사이드 프로젝트로 노트앱 (https://www.q-note.app)과 홈서버 자동 구축 솔루션인 브루넷(https://www.brewnet.dev) 등 다양한 아이디어를 AI 도구를 통해 구현하는데 재미를 느끼고 있다. 

[![GitHub](https://img.shields.io/badge/GitHub-villainscode-181717?logo=github)](https://github.com/villainscode)
[![Email](https://img.shields.io/badge/Email-villainscode@gmail.com-EA4335?logo=gmail&logoColor=white)](mailto:villainscode@gmail.com)

</td>
<td width="50%" valign="top">

#### 백승현 (Seunghyun Baek)

**디스패치(Dispatch) CTO**

2002년 개발자로 커리어를 시작해 한국과 일본을 오가며 20년 이상 소프트웨어 개발 경험을 쌓았다. 일본에서 닛산자동차 웹사이트 빌드 툴, 미즈호은행 대출시스템, 상공중금 영업지원시스템 등 대규모 금융·제조 프로젝트에 리더로 참여하며 시스템 설계와 팀 리딩 경험을 쌓았다. 이후 한국으로 돌아와 YES24의 전자책 리더기 **크레마** 초기 버전 개발에 참여했다.

2014년부터 한국 최대 연예 미디어 **디스패치**의 CTO로 재직 중이다. 한국 미디어 기업 최초로 AWS 클라우드 도입을 주도했으며, 자체 CMS, 광고관리시스템, 포토/비디오 DB 등 핵심 시스템을 직접 설계·구축했다. 수천만 명이 동시 접속하는 특종 보도 상황에서도 안정적인 서비스 운영 체계를 구축하여 트래픽 대응 비용을 70% 절감했으며, 대규모 웹 트래픽 분석 툴을 개발해 데이터 기반의 미디어 운영 전략을 지원하고 있다. 2013년 공개 SW 개발자 대회 금상 수상.

[![GitHub](https://img.shields.io/badge/GitHub-pekuid-181717?logo=github)](https://github.com/pekuid)
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
| **3** | 중급편 | AWS Bedrock 기반 AI 챗봇 — 스트리밍, 컨텍스트 관리, Tool Use, Docker 배포 |
| **4** | 실전 노하우 | 고급 활용 기법, 할루시네이션 대응, 대규모 코드베이스 전략, 팀 협업 |

**핵심 철학**: *도구는 바뀌어도 원칙은 변하지 않는다.* 이 책의 방법론은 Claude Code, Cursor, Copilot, Codex, 그 어떤 AI 코딩 에이전트에도 그대로 적용할 수 있습니다.

---

### 📬 연락처

책 또는 이 조직에 대한 문의는 저자 이메일 또는 GitHub를 통해 연락해 주세요.

---

<div align="center">

*"AI 코딩 도구를 '쓸 줄 아는' 것과 '잘 활용하는' 것 사이에는 큰 차이가 있다."*

</div>
