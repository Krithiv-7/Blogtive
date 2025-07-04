# 🌟 Blogtive — Ultra-Detailed Roadmap

This document describes every phase, task, validation, and consideration for developing Blogtive to completion.  
All features are assumed to be **opt-in (optional)** where applicable and controlled through `.env`.

---

## 📜 Vision

Blogtive is a modern, scalable content management platform designed for creators and teams.  
It delivers fast, SEO-optimized blogs with a polished admin panel, fine-grained RBAC, markdown-driven content creation, and optional integrations for advanced workflows.

Tech stack:
- **Backend**: Node.js (LTS) + TypeScript, Express, GraphQL/REST hybrid, Prisma ORM
- **Frontend**: React + TypeScript, TailwindCSS, Vite
- **Database**: SQLite (dev), PostgreSQL/MySQL (prod)
- **Optional services**: Redis, OAuth, Email, Discord Bot, Analytics, Slack, Search, Monitoring

---

# 📦 Phase 0 — Project Setup & Developer Environment

🎯 *Goal: establish monorepo, tools, and documentation to enable consistent development.*

### Tasks:
- [ ] Initialize **Git repository** and push to GitHub/other
- [ ] Create `.gitignore`:
  - `node_modules/`, `.env`, `.next/`, `dist/`, `coverage/`, `logs/`, `uploads/`, `.DS_Store`
- [ ] `.nvmrc` with latest Node LTS version (`20.11.1`)
- [ ] Root `package.json` with Yarn/NPM workspaces:
  - `server/`
  - `client/`
  - `frontend-demo/`
- [ ] Add `.env.example`:
  - Document all keys, expected values, defaults
  - Include placeholders for secrets
  - Include supported options (`light|dark|system`, `smtp|sendgrid`, etc.)

### Developer Experience:
- [ ] ESLint + Prettier + editorconfig with clear rules
- [ ] Husky pre-commit hooks
  - Run `lint-staged` for staged files
  - Run `tsc --noEmit`
- [ ] CI/CD pipeline (GitHub Actions) to:
  - Run lint
  - Run unit tests
  - Build frontend & backend
  - Optionally deploy to staging branch
- [ ] Add `.vscode/settings.json` for workspace-level hints
- [ ] Add changelog & commit conventions (Conventional Commits)

### Documentation:
- [ ] `README.md`:
  - Installation
  - Running dev servers
  - Tech stack diagram
  - Contribution guidelines
  - Roadmap & issues link
- [ ] `ROADMAP.md` & `TASKS.md`
- [ ] `CONTRIBUTING.md`

✅ *Deliverable: CI pipeline passes, `.env.example` complete, clean monorepo.*

---

# 🎨 Phase 1 — UI/UX Prototype

🎯 *Goal: validate UX and layout using static HTML/CSS/JS prototype.*

### Tasks:
- [ ] Create `frontend-demo/`
- [ ] Integrate TailwindCSS via CDN
- [ ] Define **color palette & typography**:
  - Heading hierarchy
  - Button states
  - Alerts & notifications
- [ ] Build **base layouts**:
  - Header: logo (light/dark), site title, theme toggle, user menu
  - Footer: copyright
  - Sidebar: dynamic nav links (per role)
  - Breadcrumb component
- [ ] Build static pages:
  - Auth: Login, Register, Forgot Password
  - Dashboards: Admin, Moderator, Editor, Author, Member
  - Content: Post List, Post Detail, Post Editor (with markdown preview)
  - Categories & Tags
  - Comments moderation
  - Media uploads
  - Settings: Site Settings, User Profile
  - Optional services: Redis, Discord Bot, Analytics, Slack, Search
- [ ] Test light & dark mode toggle
- [ ] Make responsive & test on all breakpoints
- [ ] Accessibility:
  - Keyboard navigation
  - ARIA attributes
  - Contrast ratio checks
- [ ] Export screenshots for approval

✅ *Deliverable: navigable static prototype with documented interactions & UX notes.*

---

# 🔧 Phase 2 — Backend MVP

🎯 *Goal: implement database models, APIs, auth, RBAC, and optional service stubs.*

### Setup:
- [ ] Initialize `server/` with TypeScript
- [ ] Install dependencies: express, apollo-server-express, graphql, prisma, bcrypt, jsonwebtoken, multer
- [ ] Install dev tools: `ts-node-dev`, `typescript`, `@types/*`
- [ ] `.env` loader & runtime validator

### Database:
- [ ] Prisma models:
  - User, Role, Post, Category, Tag, Comment, Media
  - Include fields for SEO metadata (title, description, slug)
  - Timestamps & soft-deletes
- [ ] Run migrations
- [ ] Seed:
  - Default roles: Admin, Moderator, Editor, Author, Member
  - Admin user
  - Sample categories & tags
- [ ] Write database test script

### Auth & RBAC:
- [ ] JWT-based login, registration, refresh token
- [ ] RBAC middleware
- [ ] Dynamic role builder:
  - Create/edit/delete roles
  - Assign permissions
  - Assign users

### CRUD services:
- [ ] User management (admin & moderator)
- [ ] Posts:
  - Drafts, scheduled, published
  - Autosave & revision history
- [ ] Categories & tags
- [ ] Comments moderation queue
- [ ] Media uploads:
  - Store file path
  - Validate file types & size from `.env`

### APIs:
- [ ] GraphQL schema:
  - Queries & mutations
  - Pagination & filtering
- [ ] REST endpoints:
  - `/api/upload`
  - `/api/roles`
  - `/api/users`
  - `/api/webhook/discord`
  - `/api/health`

### Optional services (all gated by `.env`):
- [ ] Redis caching
- [ ] Email service (SMTP/Sendgrid/Mailgun)
- [ ] OAuth (Google, GitHub, Twitter)
- [ ] Discord bot
- [ ] Analytics hooks
- [ ] Slack webhook
- [ ] Search with Algolia
- [ ] Monitoring with Sentry

### Security:
- [ ] Helmet
- [ ] Rate limiting
- [ ] XSS/CSRF checks
- [ ] Logging with Winston or Pino

✅ *Deliverable: fully working backend with auth, RBAC, GraphQL & REST APIs, and all services stubbed & toggleable.*

---

# 🌐 Phase 3 — Frontend MVP

🎯 *Goal: build production-ready React frontend integrated with backend APIs.*

### Setup:
- [ ] Initialize `client/` with Vite + React + TypeScript
- [ ] Install TailwindCSS, Axios, Apollo Client
- [ ] `.env` for API base URL & other settings

### Core flows:
- [ ] Auth:
  - Login, register, forgot/reset password
  - JWT persistence
  - OAuth flows (when enabled)
- [ ] Role-based dashboards:
  - Admin: full control
  - Moderator: user/comments moderation
  - Editor: posts & SEO
  - Author: personal drafts & posts
  - Member: personalized feed
- [ ] Pages:
  - Posts list & detail
  - Post editor with markdown & preview
  - Categories & tags
  - Comments moderation
  - Media upload & library
  - Site settings & profile

### Optional services screens:
- [ ] Redis, Discord bot, Analytics, Slack, Search

### UI polish:
- [ ] Theme toggle
- [ ] Responsive & accessible
- [ ] Unit test reusable components

✅ *Deliverable: fully functional, role-based frontend MVP integrated with backend.*

---

# 🧩 Phase 4 — Optional Services

🎯 *Goal: enable & validate each optional integration.*

### Tasks:
- [ ] Redis: enable, validate cache hit/miss
- [ ] Email: test email delivery
- [ ] OAuth: test Google, GitHub, Twitter
- [ ] Discord bot: validate commands & hooks
- [ ] Analytics: validate metrics collection
- [ ] Slack: test notifications
- [ ] Search: validate search results & indexing
- [ ] Sentry: test error reporting

✅ *Deliverable: all optional services functional & reflected in admin panel.*

---

# 🚀 Phase 5 — Production Hardening

🎯 *Goal: make system ready for production.*

### Tasks:
- [ ] Write unit & integration tests (coverage >80%)
- [ ] Finalize CI/CD pipeline:
  - Run tests & build
  - Deploy to staging/prod
- [ ] HTTPS & SSL certs
- [ ] SEO:
  - robots.txt
  - sitemap.xml
  - OpenGraph & Twitter meta
- [ ] Monitoring:
  - Uptime checks
  - Error tracking (Sentry)
- [ ] Deployment scripts:
  - Dockerfile
  - PM2/k8s manifests
- [ ] Production `.env` and secrets management

✅ *Deliverable: production deployment live with monitoring.*

---

# 🔄 Phase 6 — Post-Launch Iteration

🎯 *Goal: enhance product based on feedback.*

### Tasks:
- [ ] Advanced analytics dashboards
- [ ] Plugin & theme marketplace
- [ ] Community documentation
- [ ] New APIs & integrations
- [ ] Performance tuning

✅ *Deliverable: continuous feature delivery & improvements.*

---

