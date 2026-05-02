# SimpleHabits — Minimal Habit Tracker & Journal

A clean, **local-first** habit tracker and daily journal. Track rituals, reflect on your day and visualize progress — all stored privately on your device.

> 🔒 **Privacy by design**: No accounts, no servers, no analytics. Your data never leaves your browser.

---

## Features

- **Habit tracking** with a beautiful year grid view and animated check circles
- **Daily journal** with encrypted entries (AES‑GCM via Web Crypto)
- **Analytics** dashboard for streaks, completion rates and trends
- **Dark mode by default** with one-click light theme toggle
- **Year navigation**  jump to any year for habits and journal
- Premium glassmorphic UI, smooth Framer Motion animations
- Strict CSP, input validation (Zod), rate limiting, error boundaries
- Fully responsive, mobile-friendly
- Offline ready, works without an internet connection

---

## Tech Stack

- **Framework**: React 18 + Vite 5 + TypeScript 5
- **Styling**: Tailwind CSS v3 + shadcn/ui
- **Animations**: Framer Motion
- **Local Database**: SQLite via `sql.js` (persisted in IndexedDB)
- **Encryption**: Web Crypto API (AES-GCM)
- **Validation**: Zod
- **Routing**: React Router

---

## 🚀 Run Locally

### Prerequisites
- **Node.js** 18+ (LTS recommended) — [download](https://nodejs.org/)
- **npm**, **bun**, **pnpm** or **yarn**

### Steps

```bash
# 1. Clone the repository
git clone git@github.com:Aaditya-Magar/SimpleHabitsTracker.git
cd SimpleHabitsTracker-main

# 2. Install dependencies
npm install
# or: bun install / pnpm install / yarn

# 3. Start the dev server
npm run dev

# 4. Open the app
# Vite will print a local URL, typically:
# → http://localhost:8080
```

### Available Scripts

| Command | Purpose |
|---|---|
| `npm run dev` | Start the development server with HMR |
| `npm run build` | Production build (minified, console-stripped) → `dist/` |
| `npm run build:dev` | Development-mode build (unminified, for debugging) |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint |
| `npm run test` | Run Vitest test suite once |
| `npm run test:watch` | Run Vitest in watch mode |

---


## 🔐 Privacy & Security

- **All data is stored locally** in your browser (SQLite + IndexedDB). Nothing is uploaded anywhere.
- **Journal entries are encrypted at rest** using AES-GCM (Web Crypto API).
- **Strict Content Security Policy** prevents XSS and external script injection.
- **Input validation** with Zod schemas + sanitization on every write.
- **Rate limiting** on UI actions to prevent abuse and accidental rapid writes.
- **Error boundaries** catch crashes without corrupting data.
- **Console logs and debugger statements** are stripped from production builds.

> Clearing your browser data will erase your habits and journal. Use the in-app **Export** option to back up your data.

---

## 📁 Project Structure

```
src/
├── components/      # Reusable UI (Layout, ErrorBoundary, PrivacyNotice, ui/)
├── pages/           # Routes: Habits, Journal, Analytics, Settings
├── lib/             # db.ts, crypto.ts, security.ts, theme.ts
├── hooks/           # Custom React hooks
├── index.css        # Design tokens (HSL semantic colors)
└── main.tsx         # App entrypoint
```

---

## 🤝 Contributing

Feel free to fork, customize and make it your own.

---

## 📄 License

MIT — use freely.
