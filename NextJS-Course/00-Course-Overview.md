---
title: Next.js Learning Course - Complete Curriculum
tags: []
created: '2026-09-19'
source: VaultAgent
---
# Next.js Learning Course - Complete Curriculum

> **Prerequisites**: TypeScript, React, HTML, CSS, Git, Terminal ✓
> **Target**: Production-ready Next.js developer
> **Approach**: Learn by building → Document in Obsidian → Iterate

---

## 📚 Course Structure

### Phase 1: Foundations (Week 1-2)
| Module | Topic | Note | Project |
|--------|-------|------|---------|
| 1.1 | **Next.js Architecture & Mental Model** | `01-Foundations/01-Architecture.md` | — |
| 1.2 | **App Router vs Pages Router** | `01-Foundations/02-Router-Comparison.md` | — |
| 1.3 | **Project Setup & Tooling** | `01-Foundations/03-Setup-Tooling.md` | ✅ Initialize repo |
| 1.4 | **File-System Routing Deep Dive** | `01-Foundations/04-Routing.md` | 📝 Blog scaffold |
| 1.5 | **Layouts, Templates & Route Groups** | `01-Foundations/05-Layouts.md` | 📝 Shared UI |

### Phase 2: Rendering & Data Fetching (Week 2-3)
| Module | Topic | Note | Project |
|--------|-------|------|---------|
| 2.1 | **Server Components (RSC) Fundamentals** | `02-Rendering/01-Server-Components.md` | — |
| 2.2 | **Client Components & 'use client'** | `02-Rendering/02-Client-Components.md` | 📝 Interactive island |
| 2.3 | **Data Fetching: fetch(), cache, revalidate** | `02-Rendering/03-Data-Fetching.md` | 📝 Blog with CMS |
| 2.4 | **Streaming & Suspense Boundaries** | `02-Rendering/04-Streaming.md` | 📝 Dashboard shell |
| 2.5 | **Static vs Dynamic Rendering** | `02-Rendering/05-Rendering-Modes.md` | 📝 Hybrid page |

### Phase 3: Advanced Routing & Navigation (Week 3-4)
| Module | Topic | Note | Project |
|--------|-------|------|---------|
| 3.1 | **Dynamic Routes & Params** | `03-Routing/01-Dynamic-Routes.md` | 📝 Blog post pages |
| 3.2 | **Parallel & Intercepting Routes** | `03-Routing/02-Advanced-Routing.md` | 📝 Modal/Photo view |
| 3.3 | **Navigation: Link, useRouter, prefetching** | `03-Routing/03-Navigation.md` | — |
| 3.4 | **Middleware & Edge Runtime** | `03-Routing/04-Middleware.md` | 🔐 Auth guard |
| 3.5 | **Route Handlers (API Routes v2)** | `03-Routing/05-Route-Handlers.md` | 📝 Contact form API |

### Phase 4: State, Forms & Mutations (Week 4-5)
| Module | Topic | Note | Project |
|--------|-------|------|---------|
| 4.1 | **Server Actions & Mutations** | `04-State/01-Server-Actions.md` | 📝 Create/Edit posts |
| 4.2 | **Forms: React Hook Form + Zod + Server Actions** | `04-State/02-Forms.md` | 📝 Full CRUD |
| 4.3 | **Optimistic UI & useOptimistic** | `04-State/03-Optimistic.md` | 📝 Like/Bookmark |
| 4.4 | **Client State: Zustand/Jotai + Server State: TanStack Query** | `04-State/04-State-Management.md` | 📝 Complex dashboard |
| 4.5 | **Authentication: NextAuth.js v5 (Auth.js)** | `04-State/05-Auth.md` | 🔐 Full auth flow |

### Phase 5: Database & ORM (Week 5-6)
| Module | Topic | Note | Project |
|--------|-------|------|---------|
| 5.1 | **Database Options: Postgres, SQLite, PlanetScale** | `05-Database/01-DB-Options.md` | — |
| 5.2 | **Prisma ORM: Schema, Migrations, Client** | `05-Database/02-Prisma.md` | 📝 Schema design |
| 5.3 | **Drizzle ORM Alternative** | `05-Database/03-Drizzle.md` | — |
| 5.4 | **Connection Pooling & Edge Compatibility** | `05-Database/04-Edge-DB.md` | — |
| 5.5 | **Seeding, Testing, CI/CD for DB** | `05-Database/05-DB-Workflow.md` | ✅ Pipeline |

### Phase 6: Performance & Optimization (Week 6-7)
| Module | Topic | Note | Project |
|--------|-------|------|---------|
| 6.1 | **Image Optimization & next/image** | `06-Performance/01-Images.md` | 📝 Gallery |
| 6.2 | **Font Optimization & next/font** | `06-Performance/02-Fonts.md` | — |
| 6.3 | **Bundle Analysis & Code Splitting** | `06-Performance/03-Bundle.md` | 📊 Analyze |
| 6.4 | **Caching Strategies: Full Route, Data, Router Cache** | `06-Performance/04-Caching.md` | 📝 Tune blog |
| 6.5 | **Core Web Vitals & Lighthouse CI** | `06-Performance/05-CWV.md` | ✅ CI gate |

### Phase 7: Testing & Quality (Week 7-8)
| Module | Topic | Note | Project |
|--------|-------|------|---------|
| 7.1 | **Unit Testing: Vitest + React Testing Library** | `07-Testing/01-Unit.md` | ✅ Test utils |
| 7.2 | **Integration Testing: Server Actions, API** | `07-Testing/02-Integration.md` | ✅ Test actions |
| 7.3 | **E2E Testing: Playwright** | `07-Testing/03-E2E.md` | ✅ Critical flows |
| 7.4 | **Type Safety: Strict TS, tRPC/Type-safe APIs** | `07-Testing/04-Type-Safety.md` | — |
| 7.5 | **Linting, Formatting, Husky, Commitlint** | `07-Testing/05-DX-Tooling.md` | ✅ Pre-commit |

### Phase 8: Deployment & Production (Week 8-9)
| Module | Topic | Note | Project |
|--------|-------|------|---------|
| 8.1 | **Vercel Deployment & Platform Features** | `08-Deployment/01-Vercel.md` | 🚀 Deploy |
| 8.2 | **Docker & Self-Hosting (Standalone Output)** | `08-Deployment/02-Docker.md` | 🐳 Containerize |
| 8.3 | **Environment Variables & Secrets Management** | `08-Deployment/03-Env-Secrets.md` | 🔐 Configure |
| 8.4 | **Monitoring: Sentry, LogRocket, Vercel Analytics** | `08-Deployment/04-Monitoring.md` | 📊 Observe |
| 8.5 | **Scaling: ISR, Edge, Serverless Functions** | `08-Deployment/05-Scaling.md` | — |

### Phase 9: Advanced Patterns (Week 9-10)
| Module | Topic | Note | Project |
|--------|-------|------|---------|
| 9.1 | **Internationalization (i18n) & Routing** | `09-Advanced/01-i18n.md` | 🌍 Multi-lang |
| 9.2 | **Micro-frontends & Module Federation** | `09-Advanced/02-Microfrontends.md` | — |
| 9.3 | **Real-time: WebSockets, Server-Sent Events, Pusher** | `09-Advanced/03-Realtime.md` | 💬 Chat widget |
| 9.4 | **Custom Server & Express Integration** | `09-Advanced/04-Custom-Server.md` | — |
| 9.5 | **Next.js Internals: Compiler, Turbopack, Build Output** | `09-Advanced/05-Internals.md` | — |

### Phase 10: Capstone Project (Week 10-12)
| Milestone | Deliverable | Note |
|-----------|-------------|------|
| 10.1 | **Project Spec & Architecture Decision Records (ADRs)** | `10-Capstone/01-Spec.md` |
| 10.2 | **Database Schema & API Design** | `10-Capstone/02-Schema.md` |
| 10.3 | **Core Features Implementation** | `10-Capstone/03-Implementation.md` |
| 10.4 | **Testing, CI/CD, Deployment** | `10-Capstone/04-Deploy.md` |
| 10.5 | **Post-Mortem & Retrospective** | `10-Capstone/05-Retro.md` |

---

## 🎯 Learning Methodology

### For Each Module:
1. **Read** → Official docs + 1-2 curated articles
2. **Code** → Build the mini-project in `/projects` folder
3. **Note** → Create atomic note in Obsidian (this vault)
4. **Link** → Connect to previous concepts via `[[wikilinks]]`
5. **Review** → Spaced repetition: revisit notes at 1d, 1w, 1m

### Note Template (use for every module):
```markdown
---
title: "Module Title"
tags: [nextjs, phase-X, topic]
aliases: []
---

# Module Title

## 🎯 Learning Objectives
- [ ] Objective 1
- [ ] Objective 2

## 📖 Key Concepts
- Concept → [[Linked Note]]

## 💻 Code Patterns
```tsx
// Canonical pattern
```

## ⚠️ Gotchas & Pitfalls
- Gotcha 1
- Gotcha 2

## 🔗 Related Notes
- [[Previous Module]]
- [[Next Module]]
- [[External Resource]]

## 📝 Mini-Project Notes
- What worked
- What didn't
- Questions for later
```

---

## 📂 Vault Structure
```
NextJS-Course/
├── 00-Course-Overview.md          ← YOU ARE HERE
├── 01-Foundations/
├── 02-Rendering/
├── 03-Routing/
├── 04-State/
├── 05-Database/
├── 06-Performance/
├── 07-Testing/
├── 08-Deployment/
├── 09-Advanced/
├── 10-Capstone/
└── Projects/                      ← Code lives here (gitignored in vault)
    ├── phase-1-blog-scaffold/
    ├── phase-2-cms-blog/
    └── ...
```

---

## 🚀 Getting Started

**Next Step**: Create `01-Foundations/01-Architecture.md` and start Phase 1.

```bash
# Initialize the course repo (outside vault)
mkdir nextjs-course && cd nextjs-course
git init
npx create-next-app@latest . --typescript --tailwind --eslint --app --src-dir --import-alias "@/*" --use-npm
```

---

## 📌 Progress Tracker

- [ ] Phase 1: Foundations
- [ ] Phase 2: Rendering & Data Fetching
- [ ] Phase 3: Advanced Routing
- [ ] Phase 4: State, Forms & Auth
- [ ] Phase 5: Database & ORM
- [ ] Phase 6: Performance
- [ ] Phase 7: Testing
- [ ] Phase 8: Deployment
- [ ] Phase 9: Advanced Patterns
- [ ] Phase 10: Capstone Project

---

## 🔗 Quick Links
- [[NextJS-Course/01-Foundations/01-Architecture|Start Phase 1 →]]
- [Next.js Official Docs](https://nextjs.org/docs)
- [React Server Components RFC](https://github.com/reactjs/rfcs/blob/main/text/0188-server-components.md)
- [Next.js GitHub](https://github.com/vercel/next.js)
