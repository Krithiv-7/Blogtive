# 📝 Blogtive

**Modern, scalable, and open-source CMS for creators & teams.**  
Blogtive lets you build fast, beautiful, SEO-optimized blogs with role-based workflows, optional integrations, and full control over your content and experience.

🌟 Built with Node.js, React, TypeScript, SQL & TailwindCSS.

---

## 🚀 Features

✅ Markdown editor with live preview  
✅ SEO-friendly categories, tags & pages  
✅ Drafts, autosave & scheduling  
✅ Role-based dashboards (Admin, Moderator, Editor, Author, Member)  
✅ Dynamic role builder for custom roles  
✅ Light/dark mode & themeable UI  
✅ Optional integrations: OAuth, Redis, Discord bot, analytics, monitoring  
✅ Developer-friendly with REST & GraphQL APIs  

For a full feature breakdown, see:  
📖 [OVERVIEW.md](./OVERVIEW.md)

---

## 📦 Tech Stack

| Layer                | Technology |
|----------------------|------------|
| Frontend             | React + TypeScript + Tailwind |
| Backend              | Node.js + TypeScript + Express |
| Database             | Prisma ORM + SQLite / PostgreSQL / MySQL |
| Auth                 | JWT + bcrypt + optional OAuth |
| Caching (optional)   | Redis |
| Analytics (optional) | Google Analytics / Plausible |
| Bot (optional)       | Discord |
| Monitoring (optional)| Sentry |

---

## 🧰 Getting Started

### Prerequisites
- Node.js (LTS — see `.nvmrc`)
- npm or Yarn
- SQLite (default) or a running PostgreSQL/MySQL server (optional)

### Setup
1️⃣ Clone the repository:
```bash
git clone https://github.com/krithiv-7/blogtive.git
cd blogtive
```

2️⃣ Install dependencies:
```bash
npm install
```

3️⃣ Configure your environment:
```bash
cp .env.example .env
# Then edit .env with your preferred settings
```

4️⃣ Set up the database:
```bash
npx prisma migrate dev --name init
```

5️⃣ Run the development servers:
```bash
npm run dev
```

Frontend: [http://localhost:3000](http://localhost:3000)  
Backend: [http://localhost:4000](http://localhost:4000)

---

## 🤝 Contributing

We welcome contributions from everyone! 🙌  
Please read:
- [CONTRIBUTING.md](./CONTRIBUTING.md)
- [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md)

If you find a security issue, please report it privately:  
- [Security Policy](./SECURITY.md)

---

## 🌐 Community

💬 Discuss & report issues: [https://community.krithiv.dev](https://community.krithiv.dev)  
💬 Chat with us: [https://discord.krithiv.dev](https://discord.krithiv.dev)

---

## 📜 License

Blogtive is open-source software licensed under the MIT license.  
See [LICENSE](./LICENSE) for details.

---

✨ Made with ❤️ by [Krithiv-7](https://krithiv.dev) and contributors.
