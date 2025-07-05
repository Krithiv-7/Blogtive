blogtive/
├── .editorconfig               # EditorConfig for consistent style
├── .env                        # Environment variables (not committed)
├── .env.example                # Example .env file to copy and edit
├── .gitignore                  # Git ignore rules
├── .nvmrc                      # Node.js version file
├── .prettierrc                 # (optional) Prettier configuration
├── .vscode/                    # VS Code team settings
│   └── settings.json
├── CODE_OF_CONDUCT.md          # Code of conduct for contributors
├── CONTRIBUTING.md             # Contribution guidelines
├── LICENSE.md                  # Open-source license
├── OVERVIEW.md                 # Full project overview/spec
├── README.md                   # Project introduction & quickstart
├── SECURITY.md                 # Security reporting policy
├── STRUCTURE.md                # (this file) Directory structure doc
├── package.json                # Root package.json for monorepo scripts
├── tsconfig.json               # Base TypeScript config
├── docs/                       # Documentation (MkDocs / Markdown)
│   ├── index.md
│   └── ...
├── tests/                      # Global tests
│   ├── integration/
│   ├── unit/
│   └── e2e/
│
├── client/                     # React frontend app
│   ├── public/                 # Static assets (favicon, logos, manifest)
│   │   ├── favicon.ico
│   │   ├── logo-light.png
│   │   ├── logo-dark.png
│   │   └── ...
│   ├── src/
│   │   ├── assets/            # Images, fonts, etc.
│   │   ├── components/        # Shared React components
│   │   ├── contexts/          # React Contexts (theme, auth, etc.)
│   │   ├── hooks/             # Custom hooks
│   │   ├── layouts/           # Layout components (dashboard, auth, etc.)
│   │   ├── pages/             # Route pages
│   │   │   ├── index.tsx
│   │   │   ├── dashboard.tsx
│   │   │   └── ...
│   │   ├── styles/            # Tailwind & global styles
│   │   ├── utils/             # Helper functions
│   │   └── main.tsx           # Entry point
│   ├── package.json
│   ├── tailwind.config.js
│   └── tsconfig.json
│
├── server/                     # Node.js backend app
│   ├── prisma/                 # Prisma schemas & migrations
│   │   ├── schema.prisma
│   │   └── migrations/
│   ├── src/
│   │   ├── api/               # REST & GraphQL handlers
│   │   ├── auth/              # Auth logic (JWT, OAuth)
│   │   ├── bots/              # Discord bot integration
│   │   ├── cache/             # Redis integration
│   │   ├── config/            # Configuration loader
│   │   │   ├── index.ts
│   │   │   └── env.ts
│   │   ├── controllers/       # Controllers for API endpoints
│   │   ├── middlewares/       # Express middlewares
│   │   ├── models/            # Prisma models & DB utilities
│   │   ├── routes/            # Express routes
│   │   ├── services/          # Business logic services
│   │   ├── utils/             # Utility functions
│   │   ├── index.ts           # Server entry point
│   │   └── app.ts             # Express app setup
│   ├── package.json
│   └── tsconfig.json
│
├── frontend-demo/              # Static HTML/CSS/JS UI prototype
│   ├── index.html
│   ├── css/
│   └── js/
│
└── uploads/                    # Media uploads (runtime, not versioned)
