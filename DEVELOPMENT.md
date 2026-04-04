# Developer Setup

Get up and running on any House by Wokspec repo.

---

## Prerequisites

- **Node.js 20+** — [nvm](https://github.com/nvm-sh/nvm) recommended: `nvm use 20`
- **pnpm** — some repos use pnpm workspaces: `npm i -g pnpm`
- **Git** with SSH configured for GitHub
- **GitHub CLI** (`gh`) — for PR workflows

---

## Quick Start

```bash
git clone git@github.com:ws-house/<repo>.git
cd <repo>
npm ci          # or: pnpm install
npm run dev
```

---

## Repos

| Repo | Stack | Notes |
|------|-------|-------|
| [chopsticks](https://github.com/ws-house/chopsticks) | Node.js, discord.js | Discord bot |
| [nqita-cli](https://github.com/ws-house/nqita-cli) | TypeScript, Node.js | Local daemon + CLI |
| [lidock](https://github.com/ws-house/lidock) | TypeScript, React, pnpm workspace | Dock runtime monorepo |
| [token-tengu](https://github.com/ws-house/token-tengu) | TypeScript, Node.js | CLI tool |

---

## Commit Format

All House by Wokspec repos use **conventional commits**. The `commit-msg` hook rejects non-conforming commits.

```
<type>: <description>

Types: feat  fix  docs  style  refactor  perf  test  chore  ci
```

Examples:
```bash
git commit -m "feat: add adapter interface to nqita-cli"
git commit -m "fix: resolve import path in lidock core"
git commit -m "chore: update typescript to 5.5"
```

Header max 100 characters. No sentence-case, PascalCase, or UPPER_CASE in the description.

---

## Branches

Use the type as your branch prefix:

```bash
git checkout -b feat/adapter-system
git checkout -b fix/dock-layout-overflow
git checkout -b chore/update-deps
```

---

## PR Workflow

1. Push your branch
2. Open a PR
3. CI (type-check, lint, tests) must be green
4. Get a review, then merge

---

## Getting Help

- Open an issue in the relevant repo
- Email [hello@wokspec.org](mailto:hello@wokspec.org)
