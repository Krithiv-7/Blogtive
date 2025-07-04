# 📖 Blogtive — Project Overview

**Blogtive** is an open-source, modern content management platform designed for **creators, writers, and collaborative teams**.  
It combines a beautiful, responsive user interface with a scalable backend, allowing full control over content, structure, SEO, roles, and integrations — while remaining flexible and developer-friendly.

---

## 🌟 Vision

✅ Empower individuals and teams to publish high-quality, SEO-optimized content  
✅ Support multi-author workflows with clear roles & dashboards  
✅ Keep core functionality lightweight and performant  
✅ Provide sensible defaults but enable deep customization  
✅ Foster an inclusive and collaborative open-source community

---

## 🏗️ Architecture

Blogtive follows a **monorepo structure**, with clearly separated workspaces:

```
blogtive/
├── client/           Frontend: React + TypeScript + Tailwind
├── server/           Backend: Node.js + TypeScript + Prisma
├── frontend-demo/    Static HTML/CSS/JS prototype (UI mockups)
├── docs/             Project documentation
├── tests/            Unit, integration, and E2E tests
├── .env              Central environment configuration
├── package.json      Monorepo root
```

### Backend
- **Framework:** Node.js (LTS) + Express + TypeScript
- **Database:** Prisma ORM with SQLite (default), PostgreSQL or MySQL
- **API:** Hybrid — REST for CRUD, GraphQL for complex queries
- **Authentication:** JWT-based with optional OAuth
- **Caching:** Optional Redis integration

### Frontend
- **Framework:** React + TypeScript
- **Styling:** Tailwind CSS
- **Features:** Role-specific dashboards, light/dark mode, themeable layouts

---

## 📦 Tech Stack

| Layer                | Technology |
|----------------------|------------|
| Frontend             | React + TypeScript + Tailwind |
| Backend              | Node.js + TypeScript + Express |
| Database             | Prisma ORM + SQLite / PostgreSQL / MySQL |
| Auth                 | JWT + bcrypt + optional OAuth |
| Caching (optional)   | Redis |
| Bot (optional)       | Discord |
| Analytics (optional) | Google Analytics / Plausible |
| Monitoring (optional)| Sentry |
| Search (optional)    | Algolia |

---

## 🎨 Features

### ✍️ Content Management
- Markdown-based editor with live preview
- Categories & tags (SEO-friendly)
- Drafts, autosave, revision history
- Scheduling for future publication
- Media uploads (type, size, and path configurable)

### 👥 Roles & Dashboards
- Predefined roles: Admin, Moderator, Editor, Author, Member
- Dynamic role builder (admin can create custom roles)
- Role-specific dashboards to avoid clutter

### 🔐 Authentication
- JWT-based authentication
- Optional OAuth (Google, GitHub, X)
- Secure password storage with bcrypt

### 🔍 SEO & Analytics
- Built-in meta tags, OpenGraph, sitemaps
- Per-post SEO controls (Editors & Admin only)
- Optional analytics integrations

### 🤖 Optional Integrations
- Redis caching
- Discord bot (configurable REST API)
- Algolia search
- Slack notifications
- Monitoring via Sentry

### 🌐 Theme & UI
- Default light/dark mode with toggle
- Fully themeable (CSS/SCSS/Tailwind)
- Configurable site title, description, logos & favicon

---

## 🌐 Environment Management

Central `.env` file at the root governs all runtime configuration:
- Site metadata: title, description, logos, favicon
- Theme & UI defaults
- Database connection
- Auth secrets & OAuth credentials
- Feature toggles (`ENABLE_*` flags) for optional services
- Upload paths, limits & supported types
- Monitoring & analytics keys
- Server port, log level, maintenance mode

This design allows teams to manage most settings outside of the admin panel.

---

## 🚦 Development Workflow

### 📄 Backend
✅ Gather required dependencies & set up linting  
✅ Design DB schema & migrations (Prisma)  
✅ Implement CRUD endpoints (REST & GraphQL)  
✅ Implement auth & RBAC logic  
✅ Write tests: unit + integration  
✅ Add support for optional services

### 🎨 Frontend
✅ Create static HTML/CSS/JS prototype  
✅ Scaffold React + Tailwind app  
✅ Build shared UI components & layouts  
✅ Implement role-specific dashboards  
✅ Connect with backend APIs  
✅ Integrate theme toggle & settings

### 📦 Deployment
✅ CI/CD scripts & Dockerization  
✅ Staging & production environment configurations  
✅ Load balancer & monitoring

---

## 🧑‍💻 Contribution Guidelines

We welcome contributions!  
Please review the following documents before contributing:
- [`CONTRIBUTING.md`](CONTRIBUTING.md) — development workflow & commit conventions
- [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) — be kind & respectful
- [`SECURITY.md`](SECURITY.md) — how to report vulnerabilities
- [`LICENSE`](LICENSE) — open-source license (MIT)

---

## 📜 Roadmap

✅ Phase 1: Monorepo & environment setup  
✅ Phase 2: Database schema & migrations  
✅ Phase 3: Backend authentication & RBAC  
✅ Phase 4: Frontend UI prototype  
✅ Phase 5: React MVP frontend  
✅ Phase 6: Integrations & optional services  
✅ Phase 7: CI/CD pipeline & deployment  
✅ Phase 8: Documentation & release

---

## 🌐 Community Links

💬 Discuss & report issues: [https://community.krithiv.dev](https://community.krithiv.dev)  
💬 Chat with us: [https://discord.krithiv.dev](https://discord.krithiv.dev)

We look forward to building **Blogtive** with your ideas and contributions! 🚀

