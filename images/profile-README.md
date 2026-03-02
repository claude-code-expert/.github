<div align="center">

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/banner.png" alt="Claude Code Expert" width="100%" />

<br/><br/>

**AI-Assisted Development — Principles, Practices, and Production Code**

*AI와 함께하는 개발 — 원칙, 방법론, 그리고 실전 코드*

[![Book](https://img.shields.io/badge/Book-Claude_Code_Expert-2E75B6?style=for-the-badge&logo=bookstack&logoColor=white)](#about)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Next.js](https://img.shields.io/badge/Next.js_15-000000?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)

[English](#english) · [한국어](#한국어)

</div>

---

## English

### About

**Claude Code Expert** is the official GitHub organization for the book *"Claude Code Expert — AI-Assisted Development from Design to Deployment."*

This book goes beyond tool tutorials. It presents a comprehensive methodology for collaborating with AI coding agents — covering specification-driven development (SDD), test-driven development (TDD), and systematic review practices that remain relevant regardless of which AI tool you use.

All example code, project templates, and reference materials from the book are maintained in this organization.

### What You'll Find Here

This organization hosts the companion repositories for the book, along with open-source side projects built entirely with Claude Code. Each repository demonstrates the principles and workflows discussed in the book — from specification writing to deployment.

---

### 📦 Repositories

#### [tika](https://github.com/claude-code-expert/tika) — Ticket-based Kanban Board TODO App

The primary example project used throughout the book (Part 2). A full-stack Kanban board application built with SDD and TDD methodologies using Claude Code.

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika-screenshot.png" alt="Tika Kanban Board" width="100%" />

- **Stack**: Next.js 15 (App Router) · TypeScript · Tailwind CSS 4 · Drizzle ORM · Vercel Postgres
- **Features**: Drag-and-drop kanban board, ticket CRUD, status management, priority ordering
- **Methodology**: Complete SDD workflow — PRD → TRD → REQUIREMENTS.md → API Spec → Component Spec → Test Cases → Implementation
- **Demo**: [tika-kappa.vercel.app](https://tika-kappa.vercel.app)

#### [brewnet](https://github.com/claude-code-expert/brewnet) — Self-Hosted Home Server Bootstrapper

An open-source CLI tool that sets up a fully self-hosted home server with a single command. Built entirely with Claude Code as a real-world side project.

- **Stack**: TypeScript · Node.js · Docker Compose
- **Features**: 7-step interactive wizard, Docker auto-install, Git/DB/File/Media server setup, Cloudflare Tunnel integration for external access
- **Website**: [www.brewnet.dev](https://www.brewnet.dev)

#### [brewnet-boilerplate](https://github.com/claude-code-expert/brewnet-boilerplate) — Full-Stack Boilerplate Collection

The official boilerplate monorepo for Brewnet — 16 production-ready full-stack templates across 6 programming languages, all launchable with a single command.

- **Languages**: Go · Rust · Java · Kotlin · Node.js · Python
- **Frameworks**: Gin, Echo, Fiber, Actix-web, Axum, Spring Boot, Spring, Ktor, Express, NestJS, Next.js, FastAPI, Django, Flask
- **Features**: Uniform API contract across all stacks, multi-database support (PostgreSQL/MySQL/SQLite3), Docker multi-stage builds, management dashboard
- **Website**: [www.brewnet.dev](https://www.brewnet.dev)

> *More repositories will be added as the book progresses through its intermediate and advanced sections.*

---

### 👥 Authors

<table>
<tr>
<td width="50%" valign="top">

#### Namhee Lee (이남희)

**Server Developer at Kakao**

A 20-year software engineering veteran who has navigated the full spectrum of the industry — from enterprise WAS vendors and large-scale SI projects in commerce, telecommunications, and electronics, to building common frameworks and serving as an application architect.

After winning an award at the Korea Open Source Software Developer Contest in 2012 with an open-source project born from a study group, he joined **Coupang**, where he spent four years developing order/delivery MSA systems and travel booking services. Following roles at LF and Kakao as a cell lead, part lead, and engineering leader, he chose to return to hands-on development after witnessing the transformative potential of AI coding tools.

He currently builds side projects with Claude Code, including **[Q-Note](https://www.q-note.app)** (a note-taking app) and **[Brewnet](https://www.brewnet.dev)** (a self-hosted home server solution).

[![GitHub](https://img.shields.io/badge/GitHub-villainscode-181717?logo=github)](https://github.com/villainscode)
[![Email](https://img.shields.io/badge/Email-villainscode@gmail.com-EA4335?logo=gmail&logoColor=white)](mailto:villainscode@gmail.com)

</td>
<td width="50%" valign="top">

#### Seunghyun Baek (백승현)

**CTO at Dispatch (디스패치)**

A developer with over 20 years of experience spanning Korea and Japan. In Japan, he served as a project leader on large-scale enterprise systems including Nissan Motor's website build tools, Mizuho Bank's loan system, and Shoko Chukin Bank's sales support platform. After returning to Korea, he contributed to the early development of YES24's **Crema** e-reader.

Since 2014, he has served as CTO of **Dispatch**, Korea's largest entertainment media outlet. He pioneered AWS cloud adoption among Korean media companies, designed and built core systems including a custom CMS, ad management platform, and photo/video database. He engineered a traffic-handling architecture that reduced infrastructure costs by 70% during breaking news events with tens of millions of concurrent users, and developed large-scale web traffic analytics tools for data-driven media operations. Gold Award winner at the 2013 Korea Open Source Software Developer Contest.

[![GitHub](https://img.shields.io/badge/GitHub-pekuid-181717?logo=github)](https://github.com/pekuid)
[![Email](https://img.shields.io/badge/Email-pekuid@gmail.com-EA4335?logo=gmail&logoColor=white)](mailto:pekuid@gmail.com)

</td>
</tr>
</table>

---

### 📖 Book Overview

The book is structured in four parts, progressing from theory to practice, and from fundamentals to advanced topics:

| Part | Title | Description |
|:----:|-------|-------------|
| **1** | Getting Started | Developer paradigm shift, Claude Code setup, AI collaboration methodology (TDD, SDD, MCP) |
| **2** | Beginner | Full-stack TODO app (Tika) — requirements → design → development → testing → deployment |
| **3** | Intermediate | AI chatbot with AWS Bedrock — streaming, context management, Tool Use, Docker deployment |
| **4** | Real-World | Advanced techniques, hallucination handling, large codebase strategies, team collaboration |

**Core Philosophy**: *Tools change. Principles don't.* The methodologies in this book apply to any AI coding agent — Claude Code, Cursor, Copilot, Codex, or whatever comes next.

---

### 📬 Contact

For questions about the book or this organization, reach out to the authors via email or GitHub.

---

## 한국어

### 소개

**Claude Code Expert**는 『Claude Code Expert — 설계부터 배포까지, AI와 함께하는 개발』의 공식 GitHub 조직입니다.

이 책은 단순한 도구 사용법 튜토리얼이 아닙니다. AI 코딩 에이전트와 체계적으로 협업하는 방법론을 제시합니다 — 명세 주도 개발(SDD), 테스트 주도 개발(TDD), 그리고 어떤 AI 도구를 사용하든 변하지 않는 체계적인 리뷰 프로세스까지 다룹니다.

책에 수록된 모든 예제 코드, 프로젝트 템플릿, 참고 자료가 이 조직에서 관리됩니다.

### 이 조직에서 제공하는 것

이 조직은 책의 companion 레포지토리와 함께, Claude Code로 직접 개발한 오픈소스 사이드 프로젝트를 호스팅합니다. 각 레포지토리는 책에서 논의하는 원칙과 워크플로우를 실제로 보여줍니다 — 명세 작성부터 배포까지.

---

### 📦 레포지토리

#### [tika](https://github.com/claude-code-expert/tika) — 티켓 기반 칸반 보드 TODO 앱

책의 Part 2 전체에서 사용하는 핵심 예제 프로젝트입니다. Claude Code를 활용하여 SDD와 TDD 방법론으로 개발한 풀스택 칸반 보드 애플리케이션입니다.

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika-screenshot.png" alt="Tika 칸반 보드" width="100%" />

- **기술 스택**: Next.js 15 (App Router) · TypeScript · Tailwind CSS 4 · Drizzle ORM · Vercel Postgres
- **주요 기능**: 드래그 앤 드롭 칸반 보드, 티켓 CRUD, 상태 관리, 우선순위 정렬
- **개발 방법론**: SDD 전체 워크플로우 — PRD → TRD → REQUIREMENTS.md → API 명세 → 컴포넌트 명세 → 테스트 케이스 → 구현
- **데모**: [tika-kappa.vercel.app](https://tika-kappa.vercel.app)

#### [brewnet](https://github.com/claude-code-expert/brewnet) — 셀프호스팅 홈 서버 자동 구축 도구

단 하나의 명령어로 완전한 셀프호스팅 홈 서버를 구축하는 오픈소스 CLI 도구입니다. 실전 사이드 프로젝트로서 전체가 Claude Code로 개발되었습니다.

- **기술 스택**: TypeScript · Node.js · Docker Compose
- **주요 기능**: 7단계 대화형 위저드, Docker 자동 설치, Git/DB/파일/미디어 서버 구성, Cloudflare Tunnel 외부 접속
- **웹사이트**: [www.brewnet.dev](https://www.brewnet.dev)

#### [brewnet-boilerplate](https://github.com/claude-code-expert/brewnet-boilerplate) — 풀스택 보일러플레이트 모음

Brewnet의 공식 보일러플레이트 모노레포로, 6개 프로그래밍 언어에 걸쳐 16개의 프로덕션 레디 풀스택 템플릿을 제공합니다. 단일 명령어로 실행 가능합니다.

- **지원 언어**: Go · Rust · Java · Kotlin · Node.js · Python
- **프레임워크**: Gin, Echo, Fiber, Actix-web, Axum, Spring Boot, Spring, Ktor, Express, NestJS, Next.js, FastAPI, Django, Flask
- **주요 특징**: 전 스택 통일된 API 규약, 멀티 데이터베이스 지원 (PostgreSQL/MySQL/SQLite3), Docker 멀티스테이지 빌드, 관리 대시보드
- **웹사이트**: [www.brewnet.dev](https://www.brewnet.dev)

> *책의 중급편 및 고급편이 진행됨에 따라 더 많은 레포지토리가 추가될 예정입니다.*

---

### 👥 저자

<table>
<tr>
<td width="50%" valign="top">

#### 이남희 (Namhee Lee)

**카카오 서버 개발자**

20년 경력의 소프트웨어 엔지니어로, 업계의 다양한 분야를 두루 경험했다. 제약회사 전산실에서 첫 직장생활을 시작하여 WAS 기술 벤더를 거쳐, 커머스·통신·전자 등 대규모 SI 프로젝트에서 서비스 도메인 개발을 맡으며 공통 프레임워크 개발 담당 및 애플리케이션 아키텍트로 활약했다.

2012년 스터디 그룹에서 만든 오픈소스 프로덕트로 공개 SW 개발자 대회에 입상한 후, **쿠팡**에 입사하여 4년간 주문/배송 시스템의 MSA 분리 개발과 여행 예약 서비스 개발을 수행했다. 이후 LF를 거쳐 카카오에서 셀장, 파트장, 리더를 역임했으나, AI 코딩 도구의 잠재력을 목격한 후 실무로 복귀하여 현재는 서버 개발자로 근무하고 있다.

현재 Claude Code를 활용한 사이드 프로젝트로 **[Q-Note](https://www.q-note.app)**(노트 앱)과 **[Brewnet](https://www.brewnet.dev)**(홈 서버 자동 구축 솔루션)을 개발하며, 다양한 아이디어를 AI 도구로 구현하는 데 재미를 느끼고 있다.

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

*"There is a vast difference between knowing how to use an AI coding tool and knowing how to use it well."*

</div>
