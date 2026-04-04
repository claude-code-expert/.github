<div align="center">

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/banner.png" alt="Claude Code Expert" width="100%" />


<br/>

**AI-Assisted Development — Principles, Practices, and Production Code**

[![Book](https://img.shields.io/badge/Book-Claude_Code_Expert-2E75B6?style=for-the-badge&logo=bookstack&logoColor=white)](#about)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

**English** · [한국어](https://github.com/claude-code-expert/.github/blob/main/profile/README.ko.md)

</div>

---

### About

**Claude Code Expert** is the official GitHub organization for the book *"Claude Code Expert — AI-Assisted Development from Design to Deployment."*

This book goes beyond tool tutorials. It presents a comprehensive methodology for collaborating with AI coding agents — covering specification-driven development (SDD), test-driven development (TDD), and systematic review practices that remain relevant regardless of which AI tool you use.

All example code, project templates, and reference materials from the book are maintained in this organization.

### What You'll Find Here

This organization hosts the companion repositories for the book, along with open-source side projects built entirely with Claude Code. Each repository demonstrates the principles and workflows discussed in the book — from specification writing to deployment.

---

### 📦 Repositories

#### Book Companion Projects

#### [example](https://github.com/claude-code-expert/example) — Documentation Guide & Templates

A collection of project documentation templates and Claude Code configuration examples from the book. Includes a 3-tier documentation system (PRD → TRD → REQUIREMENTS), CLAUDE.md/AGENTS.md templates, skills, hooks, rules, and CLI cheat sheets.

- **Contents**: Document templates · Coding conventions · Skills & Hooks examples · Claude Code cheat sheet · Subagent guide
- **Highlights**: 3-tier doc structure, 12 hook scripts, 4 rule templates, external tool guides (SpecKit, SuperClaude, Vercel Agent Skills)

#### [tika](https://github.com/claude-code-expert/tika) — Ticket-based Kanban Board TODO App (Part 2)

The primary example project used throughout the book (Part 2). A full-stack Kanban board application built with SDD and TDD methodologies using Claude Code.

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika-intro.png" alt="Tika Intro" width="100%" />

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika-main.png" alt="Tika Kanban Board" width="100%" />

- **Stack**: Next.js 15 (App Router) · TypeScript · Tailwind CSS 4 · Drizzle ORM · Vercel Postgres
- **Features**: Drag-and-drop kanban board, ticket CRUD, status management, priority ordering
- **Methodology**: Complete SDD workflow — PRD → TRD → REQUIREMENTS.md → API Spec → Component Spec → Test Cases → Implementation
- **Demo**: [tika-app.vercel.app](https://tika-app.vercel.app/login)

#### [todo-app](https://github.com/claude-code-expert/todo-app) — Kanban Board TODO App (Chapter 6)

A companion Kanban board app for Chapter 6. Single-user ticket management with 4 columns (Backlog, TODO, In Progress, Done) and drag-and-drop support. 169 tests across 26 test suites.

- **Stack**: Next.js 15 · React 19 · TypeScript · Tailwind CSS 4 · Drizzle ORM · @dnd-kit
- **Features**: Ticket CRUD, drag-and-drop reordering, overdue detection, filter bar
- **Demo**: [ticket-kanban.vercel.app](https://ticket-kanban.vercel.app)

#### [chatbot](https://github.com/claude-code-expert/chatbot) — AI Chatbot with AWS Bedrock (Part 3)

A web-based AI chatbot application for Part 3 (Intermediate). Real-time streaming responses via SSE and Tool Use with AWS Bedrock Claude models.

- **Stack**: React 19 · Vite · Express 5 · TypeScript · Tailwind CSS · shadcn/ui · AWS Bedrock
- **Features**: SSE token streaming, Tool Use (calculator, time, weather), multi-session management, dark/light theme, Markdown rendering

#### [subagents](https://github.com/claude-code-expert/subagents) — Squad Agent System

Claude Code sub-agent system with 8 specialized agents for automated development workflows. One-line install, pipeline-based chaining, and OS-native notifications.

- **Agents**: review · plan · refactor · qa · debug · docs · gitops · audit
- **Features**: Model routing (Opus/Sonnet/Haiku), pipeline chaining, SubagentStart/Stop hooks, cross-platform notifications
- **Install**: `curl -sL https://raw.githubusercontent.com/claude-code-expert/subagents/main/install.sh | bash`

#### Open-Source Side Projects

#### [brewnet](https://github.com/claude-code-expert/brewnet) — Self-Hosted Home Server Bootstrapper

An open-source CLI tool that sets up a fully self-hosted home server with a single command. Built entirely with Claude Code as a real-world side project.

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/brewnet-web.png" alt="Brewnet Website" width="100%" />

- **Stack**: TypeScript · Node.js · Docker Compose
- **Features**: 7-step interactive wizard, Docker auto-install, Git/DB/File/Media server setup, Cloudflare Tunnel integration for external access
- **Website**: [www.brewnet.dev](https://www.brewnet.dev)

#### [brewnet-boilerplate](https://github.com/claude-code-expert/brewnet-boilerplate) — Full-Stack Boilerplate Collection

The official boilerplate monorepo for Brewnet — 16 production-ready full-stack templates across 6 programming languages, all launchable with a single command.

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/brewnet-boilerplate.png" alt="Brewnet Boilerplate" width="100%" />

- **Languages**: Go · Rust · Java · Kotlin · Node.js · Python
- **Frameworks**: Gin, Echo, Fiber, Actix-web, Axum, Spring Boot, Spring, Ktor, Express, NestJS, Next.js, FastAPI, Django, Flask
- **Features**: Uniform API contract across all stacks, multi-database support (PostgreSQL/MySQL/SQLite3), Docker multi-stage builds, management dashboard

#### Starter Templates

#### [nodejs](https://github.com/claude-code-expert/nodejs) — Minimal Node.js Web App

A minimal Node.js web application starter, deployable to Railway with one click.

- **Stack**: Node.js
- **Deploy**: [Railway](https://railway.app)

#### [java-spring-boot](https://github.com/claude-code-expert/java-spring-boot) — Spring Boot Starter App

A Spring Boot starter application, deployable to Railway with one click.

- **Stack**: Java · Spring Boot
- **Deploy**: [Railway](https://railway.app)

---

### 👥 Authors

<table>
<tr>
<td width="50%" valign="top">

#### Namhee Lee (이남희)

**Server Developer at Kakao**

A 20-year software engineering veteran who has navigated the full spectrum of the industry — from enterprise WAS vendors and large-scale SI projects in commerce, telecommunications, and electronics, to building common frameworks and serving as an application architect.

After winning an award at the Korea Open Source Software Developer Contest in 2012 with an open-source project born from a study group, he joined **Coupang**, where he spent four years developing order/delivery MSA systems and travel booking services. Following roles at LF and Kakao as a cell lead, part lead, and engineering leader, he chose to return to hands-on development after witnessing the transformative potential of AI coding tools.

In 2024, he published *[Developer Technical Interview Notes](https://product.kyobobook.co.kr/detail/S000216231695)* through Hanbit Media. He currently enjoys turning various ideas into reality with AI tools through side projects such as **[Q-Note](https://www.q-note.app)** (a note-taking app) and **[Brewnet](https://www.brewnet.dev)** (a self-hosted home server solution).

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

<div align="center">

*"There is a vast difference between knowing how to use an AI coding tool and knowing how to use it well."*

</div>
