# ✨ Contributing to Blogtive

Thank you for your interest in contributing to **Blogtive**!  
We welcome contributions from everyone — whether it's bug reports, feature suggestions, code, tests, or documentation.

This document describes the process for contributing to the project.

---

## 📜 Table of Contents

- [Getting Started](#getting-started)
- [Code of Conduct](#code-of-conduct)
- [Project Structure](#project-structure)
- [Development Setup](#development-setup)
- [Coding Guidelines](#coding-guidelines)
- [Commit Conventions](#commit-conventions)
- [Testing](#testing)
- [Pull Requests](#pull-requests)
- [Issues & Feature Requests](#issues--feature-requests)
- [License](#license)

---

## 🚀 Getting Started

Before you contribute:  
✅ Make sure there’s no existing issue or pull request for your change.  
✅ Open a discussion or issue if you’re unsure whether your change is needed.  
✅ Be respectful and collaborative!

---

## 🤝 Code of Conduct

We are committed to fostering a welcoming and harassment-free environment for everyone.  
Please read and follow our [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

---

## 📂 Project Structure

This project is a monorepo with the following workspaces:

```
/client/          - React + TypeScript frontend
/server/          - Node.js + TypeScript backend
/frontend-demo/   - Static HTML/CSS/JS prototype
/docs/            - Documentation
/tests/           - End-to-end and integration tests
```

---

## 🖥️ Development Setup

### 1️⃣ Prerequisites

- Node.js LTS (check `.nvmrc` for exact version)
- Yarn (or npm)
- PostgreSQL (or SQLite for local development)
- Redis (optional, for caching)
- An email account & OAuth keys (optional)

### 2️⃣ Install dependencies

```bash
yarn install
```

### 3️⃣ Set up environment variables

```bash
cp .env.example .env
# then edit `.env` with your local settings
```

### 4️⃣ Run the development servers

Backend:
```bash
cd server
yarn dev
```

Frontend:
```bash
cd client
yarn dev
```

---

## 🧹 Coding Guidelines

✅ Use **TypeScript** for all code.  
✅ Run ESLint & Prettier before submitting a PR:  

```bash
yarn lint
yarn format
```

✅ Write clear, modular, and documented code.  
✅ Follow project’s established naming conventions.  
✅ Keep functions small and focused.

---

## 📝 Commit Conventions

We use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) to automatically generate changelogs.

Examples:
- `feat: add role-based dashboard`
- `fix: correct JWT validation bug`
- `docs: update README with setup instructions`
- `refactor: simplify user service`
- `test: add coverage for auth middleware`

Run `yarn commit` if commitizen is installed, or use the format above manually.

---

## 🧪 Testing

✅ Write or update tests for your changes whenever possible.  
✅ Run all tests before submitting a PR:

```bash
yarn test
```

✅ Include tests for edge cases and error scenarios.

---

## 🔃 Pull Requests

✅ Fork the repository and create a feature branch:  
```bash
git checkout -b feat/your-feature-name
```

✅ Make sure your branch is up to date:  
```bash
git fetch upstream
git rebase upstream/main
```

✅ Push your branch and open a PR against `main` branch.

In your PR description:
- Explain the **what and why** of your changes.
- Reference related issues (`Closes #123`).
- Include screenshots or logs if UI-related.

Your PR will be reviewed, and you may be asked to make changes before it is merged.

---

## 🐞 Issues & Feature Requests

✅ Before opening a new issue:
- Check existing issues to avoid duplicates.
- Search the discussions if your topic is conceptual.

✅ When creating an issue:
- Provide clear, concise description.
- Include steps to reproduce if it’s a bug.
- Suggest a possible solution if you have one.

---

## 📄 License

By contributing, you agree that your contributions will be licensed under the same license as this project (MIT).

---

Thank you for helping make **Blogtive** better! 🎉  
We appreciate your time and effort.
