# Developer Setup Guide

Get from zero to running on any WokSpec repo in under 5 minutes.

---

## Prerequisites

- **Node.js 20+** — [nvm](https://github.com/nvm-sh/nvm) recommended: `nvm use 20`
- **Git** with SSH configured for GitHub
- **GitHub CLI** (`gh`) — for PR workflows: `brew install gh` / `apt install gh`

---

## Quick Start

```bash
# Clone any repo
git clone git@github.com:WokSpec/<repo>.git
cd <repo>

# Install deps (git hooks install automatically via husky)
npm ci

# Start dev server
npm run dev
```

The `npm ci` step runs `prepare` which installs husky git hooks automatically. After this:
- `commit-msg` hook validates conventional commit format before every commit
- `pre-commit` hook runs ESLint on staged files before every commit

---

## Repos at a Glance

| Repo | URL | Stack | Start |
|------|-----|-------|-------|
| [WokSite](https://github.com/WokSpec/WokSite) | wokspec.org | Next.js + CF Workers | `npm run dev` |
| [WokTool](https://github.com/WokSpec/WokTool) | tools.wokspec.org | Next.js + CF Workers | `npm run dev` |
| [WokGen](https://github.com/WokSpec/WokGen) | wokgen.wokspec.org | Next.js + Prisma | `cd apps/web && npm run dev` |
| [Vecto](https://github.com/WokSpec/Vecto) | vecto.wokspec.org | Next.js + Prisma | `cd apps/web && npm run dev` |
| [Eral](https://github.com/WokSpec/Eral) | eral.wokspec.org | Hono + CF Workers | `npm run dev` |
| [Dilu](https://github.com/WokSpec/Dilu) | dilu.wokspec.org | Next.js + CF Workers | `npm run dev` |
| [wokpost](https://github.com/WokSpec/wokpost) | wokpost.wokspec.org | Next.js + CF Workers + D1 | `npm run dev` |
| [Chopsticks](https://github.com/WokSpec/Chopsticks) | — | Node.js + discord.js | `npm run dev` |
| [WokAPI](https://github.com/WokSpec/WokAPI) | api.wokspec.org | Hono + CF Workers | `npm run dev` |

---

## Commit Format

All WokSpec repos enforce **conventional commits**. The `commit-msg` hook will reject non-conforming commits.

```
<type>: <description>

Types: feat  fix  docs  style  refactor  perf  test  chore  ci
```

Examples:
```bash
git commit -m "feat: add CSV export to json-tools"
git commit -m "fix: resolve CORS header on /v1/chat route"
git commit -m "chore: update eslint to v9"
git commit -m "docs: improve CLAUDE.md auth patterns"
```

**Max 100 characters** in the header. No sentence-case, PascalCase, or UPPER_CASE in the description.

---

## Branches

Use the type as your branch prefix:

```bash
git checkout -b feat/csv-export
git checkout -b fix/cors-v1-chat
git checkout -b chore/update-deps
```

---

## AI Agents

Every repo has `CLAUDE.md` (read by Claude Code, Cursor) and `.github/copilot-instructions.md` (read by GitHub Copilot). These files contain the architecture context agents need to write correct code.

**Before making a change with an AI agent**, tell it to read `CLAUDE.md` first. It will understand:
- Critical constraints (what must never change)
- Exact patterns to follow
- How to add common features step-by-step

To auto-generate a PR from an issue, add the `sweep` label to any issue.

---

## PR Workflow

1. Push your branch
2. Open a PR — the PR template will guide you
3. **Auto-labeler** applies file-path-based labels automatically
4. **CodeRabbit** reviews the PR within minutes and adds inline comments
5. **Commitlint CI** validates your commit messages
6. **CodeQL** and **Gitleaks** run security scans
7. Get a human review (if needed), then merge

For Dependabot PRs: minor/patch updates auto-merge after CI passes. You don't need to touch them.

---

## Environment Variables

Each repo has an `.env.example` or documents its vars in `CLAUDE.md`. Common variables:

| Variable | Used by | Description |
|----------|---------|-------------|
| `WOKAPI_TOKEN` | Most apps | WokSpec API auth token |
| `DATABASE_URL` | WokGen, Vecto | PostgreSQL (Neon) connection string |
| `NEXTAUTH_SECRET` | WokGen, Vecto, wokpost | NextAuth v5 secret |
| `ANTHROPIC_API_KEY` | WokGen | Claude API for Eral companion |
| `GROQ_API_KEY` | WokGen, Vecto, Eral | Groq (Llama 3.3 70B) |
| `DISCORD_BOT_TOKEN` | Chopsticks | Discord bot token |

---

## Useful Commands

```bash
# Type check
npx tsc --noEmit

# Lint
npx eslint . --max-warnings 0

# Run lint-staged manually (same as pre-commit hook)
npx lint-staged

# Validate your last commit message
npx commitlint --from HEAD~1 --to HEAD --verbose

# Check CI status on current branch
gh pr checks

# View recent workflow runs
gh run list --limit 10
```

---

## Labels Reference

PRs are auto-labeled based on changed files. Common labels:

| Label | What triggers it |
|-------|-----------------|
| `area:api` | Changes to API routes |
| `area:dashboard` | Dashboard page changes |
| `area:auth` | Auth/middleware changes |
| `new-tool` | New tool added to WokTool |
| `database` | Prisma schema / migrations |
| `infrastructure` | CI, config files |
| `dependencies` | package.json changes |
| `docs` | Markdown files |
| `stale` | Auto-applied after 30 days of inactivity |

---

## Getting Help

- Browse the [issues](https://github.com/WokSpec) or open a new one
- Read the repo's `CLAUDE.md` — it contains everything an agent (or human) needs
- Check `CONTRIBUTING.md` for the full contribution guide
