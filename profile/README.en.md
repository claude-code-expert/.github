<div align="center">

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/banner.png" alt="Claude Code Expert" width="100%" />


<br/>

**AI-Assisted Development — Principles, Practices, and Production Code**

[![Book](https://img.shields.io/badge/Book-Claude_Code_Master-2E75B6?style=for-the-badge&logo=bookstack&logoColor=white)](#about)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

**English** · [한국어](https://github.com/claude-code-expert/.github/blob/main/profile/README.md)

</div>

---

### About

<table>
<tr>
<td width="35%" align="center" valign="top">

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/cc-master.png" alt="Claude Code Master" width="100%" />

<br/>

<a href="https://product.kyobobook.co.kr/detail/S000219725328" target="_blank"><img src="https://img.shields.io/badge/Claude_Code_Master-Buy_Online-2E75B6?style=for-the-badge&logo=bookstack&logoColor=white" alt="Claude Code Master Buy Online" /></a>

</td>
<td width="65%" valign="top">

**Claude Code Expert** is the official GitHub organization for the book *"Claude Code Master — Agentic Coding Workflow: Planning, Development, and Operations All in One."*

This book goes beyond tool tutorials. It presents a comprehensive methodology for collaborating with AI coding agents — covering specification-driven development (SDD), test-driven development (TDD), and systematic review practices that remain relevant regardless of which AI tool you use.

All example code, project templates and examples, and reference materials from the book are maintained in this repository.

#### What You'll Find Here

This organization hosts the companion repositories for the book, along with open-source side projects built entirely with Claude Code. Each repository demonstrates the principles and workflows discussed in the book — from specification writing to development methods and deployment, completed together with examples.

</td>
</tr>
</table>

---

### 📦 Repositories

#### Book Companion Projects

#### [example](https://github.com/claude-code-expert/example) — Documentation Guide & Templates

A collection of project documentation templates and Claude Code configuration examples from the book. Includes essential documentation systems for Claude Code development (PRD, TRD, REQUIREMENTS), CLAUDE.md/AGENTS.md templates, skills, hooks, rules, and CLI cheat sheets.

- **Contents**: Document templates · Coding conventions · Skills & Hooks examples · Claude Code cheat sheet · Prompt engineering · Context engineering · Harness engineering and subagent descriptions and guide documents

## Skills (3)

Custom AI workflow definition files (`skills/`)

| Skill | Description |
|-------|-------------|
| `test-driven-development.md` | RED-GREEN-REFACTOR TDD workflow |
| `code-reviewer.md` | PR and code quality review (read-only) |
| `react-component.md` | React component generation based on team conventions |

## Commands (2)

Custom slash commands (`.claude/commands/`)

| Command | Description |
|---------|-------------|
| `/optimize` | Analyze codebase docs and suggest execution commands |
| `/security-checklist` | 7-category security check (input validation, SQL injection, XSS, env vars, dependencies, API, permissions) |

## Hooks (12)

Automation scripts (`.claude/hooks/`)

| Category | File | Trigger |
|----------|------|---------|
| **Security** | `block-dangerous.py` | PreToolUse — blocks `rm -rf`, `force push`, `DROP TABLE`, etc. |
| **Dependency** | `check-deps-py.py` | PreToolUse — warns on missing Python imports |
| **Formatting** | `format-ts.sh`, `format-py.sh` | PostToolUse — auto-format on save |
| **Linting** | `lint-ts.sh`, `lint-py.sh` | PostToolUse — lint on modification |
| **Testing** | `test-ts.sh`, `test-py.sh` | PostToolUse — auto-run tests |
| **Notifications** | `notify-slack.sh` | Notification/Stop — Slack webhook notification |
| **Notifications** | `notify-telegram.sh` | Notification/Stop — Telegram bot notification |
| **Config** | `settings.typescript.json`, `settings.python.json` | Language-specific hook configuration overrides |

## Rules (4)

Path-based coding rules (`.claude/rules/`)

| Rule | Path | Key Content |
|------|------|-------------|
| `api-routes.md` | `src/api/**/*.ts` | Response format, error handling, auth, Zod validation |
| `frontend.md` | `src/components/**/*.tsx` | Functional components, Tailwind, accessibility |
| `testing.md` | `**/*.test.ts` | AAA pattern, describe/it naming, mock management |
| `database.md` | `src/models/**/*.ts` | Model definitions, N+1 prevention, pagination, indexes |

## Templates (17)

Reusable configuration templates (`template/`)

| Category | File | Description |
|----------|------|-------------|
| **CLAUDE.md** | `CLAUDE.md` | Full example |
| | `CLAUDE.local.md` | Personal config (gitignored) |
| | `CLAUDE-template(Root).md` | Monorepo root |
| | `CLAUDE-template(Client).md` | Client-side |
| | `CLAUDE-template(Server).md` | Server-side |
| **AGENTS.md** | `AGENTS-Guide.md` | Writing guide |
| | `AGENTS-template.md` | Base template |
| | `AGENTS(java-back).md` | Spring Boot example |
| **Conventions** | `code-style.md` | Coding style (naming, format, types) |
| | `root-code-style.md` | Monorepo root code style |
| | `patterns.md` | Architecture patterns |
| | `client-patterns.md` | Client patterns (components, hooks, state) |
| | `server-patterns.md` | Server patterns (middleware, validation, errors) |
| | `git-workflow.md` | Git branch strategy, commits, PRs |
| | `testing.md` | Test strategy (unit, integration, E2E) |
| **Other** | `skill-template.md` | Skill writing template |
| | `settings.json` | settings.json with annotations |

## Project Docs (7)

3-tier documentation system + external tool guides (`docs/`)

| Tier | File | Description |
|------|------|-------------|
| Business | `PRD.md` | Product Requirements Document |
| Architecture | `TRD.md` | Technical Requirements Document |
| Implementation | `REQUIREMENTS.md` | AI Implementation Requirements |
| Reference | `COMMANDS.md` | Complete slash command reference |
| External Tools | `SpecKit_Guide.md` | Spec-Driven Development framework |
| | `SuperClaude_Guide.md` | Claude Code extension (30+ commands) |
| | `Vercel_Agent_Skills_Guide.md` | 17+ AI agent-compatible skill ecosystem |

## Engineering Guides (4)

Advanced learning materials (`guide/`)

| Guide | Key Content |
|-------|-------------|
| `prompt-engineering-guide.md` | Zero-shot, few-shot, CoT and other prompting techniques |
| `context-engineering-guide.md` | Designing the full context that AI sees |
| `harness-engineering-guide.md` | Agent quality assurance structure (Hooks, Rules, auto-verification) |
| `claude-code-hooks-guide.md` | Hooks system details (timing, env vars, matchers) |

## References (4)

Cheat sheets & CLI commands

| Document | Description |
|----------|-------------|
| `claude-code-cheatsheet-ko` | v2.1.91 shortcuts, commands, config, MCP, permissions (HTML/MD) |
| `claude-code-unshipped` | 23 unreleased features analysis based on npm source (HTML/MD) |
| `git_cli.md` | Essential and advanced Git commands |
| `postgres_cli.md` | PostgreSQL connection, management, CRUD, backup commands |

## Practical Tips (3)

Claude Code usage tips (`tips/`)

| Document | Description |
|----------|-------------|
| `CLAUDE-CODE-CLI-ALIAS-SETTINGS.md` | 65+ CLI flags, 20+ shell aliases, danger mode guide |
| `CLAUDE-CODE-NTFY-MOBILE-APPROVAL.md` | ntfy mobile approval notification setup |
| `lsp.md` | LSP integration — 3 methods compared (official plugin, cclsp, Serena) |

## Subagent Guide

| Document | Description |
|----------|-------------|
| `subagent/subagent.md` | Subagent concepts, internals, definition format, priority, Agent Teams comparison |

#### [tika](https://github.com/claude-code-expert/tika) — Ticket-based Kanban Board TODO App (Part 2)

The primary example project used throughout the book (Part 2). A full-stack Kanban board application built with SDD and TDD methodologies using Claude Code, developed with the goal of extending beyond the example into a SaaS service.

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika_intro.png" alt="Tika 소개" width="100%" />
<p align="center"><em>Tika Intro</em></p>

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika_main.png" alt="Tika 칸반 보드 메인" width="100%" />
<p align="center"><em>Tika Main</em></p>

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/tika_board.png" alt="Tika 칸반 대시보드" width="100%" />
<p align="center"><em>Tika Kanban board</em></p>

---

## Tech Stack

| Area | Technology |
|------|-----------|
| **Framework** | Next.js 15 (App Router) |
| **Language** | TypeScript |
| **Styling** | Tailwind CSS 4 |
| **ORM / DB** | Drizzle ORM · Vercel Postgres (Neon) |
| **Auth** | NextAuth.js v5 (Google OAuth) |

- **Features**: Drag-and-drop kanban board, ticket CRUD, status management, priority ordering
- **Methodology**: Complete SDD workflow — PRD → TRD → REQUIREMENTS.md → API Spec → Component Spec → Test Cases → Implementation
- **Website**: [tika-app.vercel.app](https://tika-app.vercel.app/login)

#### [todo-app](https://github.com/claude-code-expert/todo-app) — Kanban Board TODO App (Chapter 6)

A hands-on Kanban board app for Part 2 of Claude Code Expert. A prototype of Tika with single-user ticket management across 4 columns (Backlog, TODO, In Progress, Done) and drag-and-drop support.

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

#### Why Use It?
  Build a complete self-hosted home server with a single command (`brewnet init`) — no complex server knowledge required. External access is automated via Cloudflare Tunnel without port forwarding.
<br>
  Key Highlights
  - 8-step interactive wizard — configure Git server, DB, file server, and media server all at once
  - Auto-installs Docker even if not present (macOS + Linux)
  - 16-stack app scaffolding (`brewnet create-app`) — includes Gitea repository + Traefik routing
  - Web admin dashboard (localhost:8088) — real-time logs, deploy history, domain connection management
  - Full CLI control from backup, restore, to uninstall
  - Ultra-fast self-hosted home server setup from install to domain connection in ~3 minutes (may vary by network)
  - Direct hosting for static homepage content (GitHub, Cloudflare direct connection and internal hosting)


<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/brewnet-web.png" alt="Brewnet Website" width="100%" />

- **Stack**: TypeScript 5 · Node.js 20 · Docker Compose · Traefik · Cloudflare Tunnel · Commander.js · SQLite
- **Features**: 7-step interactive wizard, Docker auto-install, Git/DB/File/Media server setup, Cloudflare Tunnel integration for external access
- **Website**: [www.brewnet.dev](https://www.brewnet.dev)

#### [brewnet-boilerplate](https://github.com/claude-code-expert/brewnet-boilerplate) — Full-Stack Boilerplate Collection

The official boilerplate monorepo for Brewnet — 16 production-ready full-stack templates across 6 programming languages, all launchable with a single command.

<img src="https://raw.githubusercontent.com/claude-code-expert/.github/main/profile/assets/brewnet-boilerplate.png" alt="Brewnet Boilerplate" width="100%" />

- **Languages**: Go · Rust · Java · Kotlin · Node.js · Python
- **Supported Framework Boilerplates**: Gin, Echo, Fiber, Actix-web, Axum, Spring Boot, Spring, Ktor, Express, NestJS, Next.js, FastAPI, Django, Flask
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

[![Email](https://img.shields.io/badge/Email-pekuid@gmail.com-EA4335?logo=gmail&logoColor=white)](mailto:pekuid@gmail.com)

</td>
</tr>
</table>

---

### 📖 Book Overview

The book is structured in three parts, progressing from theory to practice, and from fundamentals to advanced topics:

| Part | Title | Description |
|:----:|-------|-------------|
| **1** | Getting Started | Developer paradigm shift, Claude Code setup, AI collaboration methodology (TDD, SDD, MCP) |
| **2** | Beginner | Full-stack TODO app (Tika) — requirements → design → development → testing → deployment |
| **3** | Intermediate | AI chatbot with AWS Bedrock — streaming, context management, Tool Use, advanced techniques, hallucination handling |

**Core Philosophy**: *Tools change. Principles don't.* The methodologies in this book apply to any AI coding agent — Claude Code, Cursor, Copilot, Codex, or whatever comes next.

---

### 📬 Contact

For questions about the book or this organization, reach out to the authors via email or GitHub.

---

<div align="center">

*"There is a vast difference between knowing how to use an AI coding tool and knowing how to use it well."*

</div>
