# 📋 Blogtive — TASKS.md

This file lists **all actionable tasks**, organized by development phases.

Each top-level phase is divided into granular, atomic tasks with clear intent.

---

- <input type="checkbox" disabled> Not done
- <input type="checkbox" checked disabled style="accent-color: green;"> Done


## 📦 Phase 0 — Project Setup & Developer Environment

### 🗃️ Repository Setup
- [x] Initialize Git repository and create initial commit
- [x] Create `.gitignore` for Node, React, Prisma, logs, uploads
- [x] Add `.nvmrc` with Node.js LTS version
- [ ] Set up Yarn/NPM workspaces:
  - [x] Add root `package.json`
  - [x] Add workspace `server/`
  - [x] Add workspace `client/`
  - [ ] Add workspace `frontend-demo/`
- [ ] Add `.editorconfig` for consistency
- [ ] Add `.vscode/settings.json` for team hints

### 📝 Environment Variables
- [ ] Create `.env.example` with:
  - [ ] Core site settings
  - [ ] Theme & UI options
  - [ ] Database URLs for SQLite/PostgreSQL/MySQL
  - [ ] JWT and bcrypt settings
  - [ ] Email service configs
  - [ ] OAuth client IDs/secrets
  - [ ] Redis configs
  - [ ] Discord bot token & channel
  - [ ] Analytics IDs
  - [ ] Slack webhook URL
  - [ ] File upload path, size, supported types
  - [ ] Server config
  - [ ] Monitoring (Sentry, etc.)
  - [ ] Search (Algolia)

### 🛠️ Developer Tooling
- [ ] Install ESLint + recommended config
- [ ] Install Prettier + config
- [ ] Add Husky pre-commit hook:
  - [ ] Lint staged files
  - [ ] Run type-check
- [ ] Install lint-staged
- [ ] Configure CI/CD:
  - [ ] GitHub Actions workflow
  - [ ] Run lint
  - [ ] Run tests
  - [ ] Build artifacts
  - [ ] Deploy staging branch

### 📄 Documentation
- [x] Write `README.md` with:
  - [x] Overview
  - [ ] Tech stack
  - [ ] Setup
  - [ ] Contribution guide
- [x] Write `ROADMAP.md`
- [x] Write `TASKS.md` (this file)
- [x] Write `CONTRIBUTING.md`
- [x] Define `LICENSE`

---

## 🎨 Phase 1 — UI/UX Prototype

### 🖌️ UI Toolkit
- [ ] Create `frontend-demo/`
- [ ] Add TailwindCSS via CDN
- [ ] Define color palette & typography scale

### 📄 Layout & Pages
- [ ] Header: site title, logo, theme toggle, user menu
- [ ] Footer: copyright
- [ ] Sidebar: dynamic nav links per role
- [ ] Breadcrumb component

### 👥 Auth Pages
- [ ] Login
- [ ] Register
- [ ] Forgot/reset password

### 🖥️ Dashboards
- [ ] Admin dashboard
- [ ] Moderator dashboard
- [ ] Editor dashboard
- [ ] Author dashboard
- [ ] Member dashboard

### 📝 Content Pages
- [ ] Post list
- [ ] Post detail
- [ ] Post editor with Markdown preview
- [ ] Categories
- [ ] Tags
- [ ] Comments moderation
- [ ] Media uploads
- [ ] Site settings
- [ ] User profile

### 🔗 Optional Services Screens
- [ ] Redis status
- [ ] Discord bot settings
- [ ] Analytics dashboard
- [ ] Slack notifications
- [ ] Search settings

### 🌗 UX Details
- [ ] Theme toggle
- [ ] Responsive design
- [ ] Accessibility (keyboard nav, ARIA, contrast)
- [ ] Export screenshots

---

## 🔧 Phase 2 — Backend MVP

### 🗃️ Server Setup
- [ ] Initialize `server/` with TypeScript
- [ ] Install express, apollo-server-express, graphql
- [ ] Install Prisma, bcrypt, jsonwebtoken, multer
- [ ] Install dev dependencies: `@types/*`, `ts-node-dev`

### 🗄️ Database
- [ ] Define Prisma models:
  - [ ] User
  - [ ] Role
  - [ ] Post
  - [ ] Category
  - [ ] Tag
  - [ ] Comment
  - [ ] Media
- [ ] Add SEO fields: slug, meta title, meta description
- [ ] Add timestamps & soft deletes
- [ ] Run initial migration
- [ ] Seed:
  - [ ] Default roles
  - [ ] Admin user
  - [ ] Example categories & tags

### 🔐 Auth & RBAC
- [ ] Implement JWT-based login & register
- [ ] Add JWT validation middleware
- [ ] Add RBAC middleware
- [ ] Implement dynamic role builder
- [ ] Add ability to assign/revoke roles

### CRUD Services
- [ ] Users CRUD (admin & moderator)
- [ ] Posts CRUD with drafts & scheduled publishing
- [ ] Categories CRUD
- [ ] Tags CRUD
- [ ] Comments moderation
- [ ] Media uploads & validations

### 🧩 APIs
- [ ] GraphQL schema:
  - Queries & Mutations
  - Pagination & filtering
- [ ] REST endpoints:
  - `/api/upload`
  - `/api/roles`
  - `/api/users`
  - `/api/webhook/discord`
  - `/api/health`

### 🔗 Optional Services
- [ ] Redis integration
- [ ] Email service
- [ ] OAuth (Google, GitHub, Twitter)
- [ ] Discord bot hooks
- [ ] Analytics
- [ ] Slack
- [ ] Search
- [ ] Monitoring (Sentry)

### 🛡️ Security
- [ ] Helmet
- [ ] Rate limiter
- [ ] XSS/CSRF prevention
- [ ] Logging (Winston/Pino)

---

## 🌐 Phase 3 — Frontend MVP

### ⚙️ Setup
- [ ] Initialize `client/` with Vite + React + TypeScript
- [ ] Install TailwindCSS
- [ ] Install Axios & Apollo Client
- [ ] Add `.env` for API base URL

### 🧠 State Management
- [ ] `AuthContext` for JWT persistence
- [ ] Global role & permissions context

### 👥 Role-Based Dashboards
- [ ] Admin
- [ ] Moderator
- [ ] Editor
- [ ] Author
- [ ] Member

### 📄 Content Management
- [ ] Post list & detail
- [ ] Post editor with Markdown preview
- [ ] Categories & Tags management
- [ ] Comments moderation
- [ ] Media upload & management

### ⚙️ Optional Services Screens
- [ ] Redis
- [ ] Discord bot
- [ ] Analytics
- [ ] Slack
- [ ] Search

### 🌗 UI Polish
- [ ] Theme toggle
- [ ] Accessibility pass
- [ ] Responsive testing
- [ ] Unit tests for components

---

## 🧩 Phase 4 — Optional Services

### 🔗 Services Activation
- [ ] Enable Redis and validate cache
- [ ] Test Email service delivery
- [ ] Test OAuth flows
- [ ] Validate Discord bot webhooks
- [ ] Validate Analytics metrics
- [ ] Validate Slack notifications
- [ ] Validate Search integration
- [ ] Validate Sentry error tracking

---

## 🚀 Phase 5 — Production Hardening

### 🧪 Testing
- [ ] Unit tests (backend & frontend)
- [ ] Integration tests
- [ ] End-to-end tests (Cypress)

### CI/CD
- [ ] Finalize pipelines:
  - Lint & test
  - Build
  - Deploy staging & production

### Deployment
- [ ] Configure HTTPS/SSL
- [ ] Configure Dockerfile
- [ ] Configure PM2 or Kubernetes manifests
- [ ] Set up production `.env` & secrets

### SEO
- [ ] robots.txt
- [ ] sitemap.xml
- [ ] OG & Twitter meta

### Monitoring
- [ ] Uptime checks
- [ ] Sentry errors
- [ ] Log aggregation

---

## 🔄 Phase 6 — Post-Launch Iteration

### 📊 Enhancements
- [ ] Advanced analytics dashboards
- [ ] Comments moderation queue improvements
- [ ] Plugin & theme marketplace
- [ ] Community documentation & tutorials
- [ ] Performance optimization
- [ ] Collect feedback & iterate

---
