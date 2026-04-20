# Developer Setup

Get up and running on any Mad House repo.

---

## Prerequisites

- **Node.js 22+** — [nvm](https://github.com/nvm-sh/nvm) recommended: `nvm use 22`
- **pnpm** — some repos use pnpm workspaces: `npm i -g pnpm`
- **Git** with SSH configured for GitHub
- **GitHub CLI** (`gh`) — for PR workflows

---

## Quick Start

```bash
git clone git@github.com:madebymadhouse/<repo>.git
cd <repo>
npm ci          # or: pnpm install
npm run dev
```

---

## Repos

| Repo | Stack | Notes |
|------|-------|-------|
| [agents](https://github.com/madebymadhouse/agents) | Markdown agent specs | Canonical fleet repo |
| [bot-dev-playbook](https://github.com/madebymadhouse/bot-dev-playbook) | Markdown playbook | Shared workflow and standards |
| [vps-maintenance-playbook](https://github.com/madebymadhouse/vps-maintenance-playbook) | Markdown control-plane docs | Live VPS maintenance notebook |
| [chopsticks-lean](https://github.com/madebymadhouse/chopsticks-lean) | Node.js, discord.js | Lean production bot |
| [chopsticks](https://github.com/madebymadhouse/chopsticks) | Node.js, discord.js, web | Full bot stack |
| [liquibar](https://github.com/madebymadhouse/liquibar) | TypeScript, React, pnpm workspace | Dock runtime monorepo |

---

## Commit Format

All Mad House repos use **conventional commits**.

```
<type>: <description>

Types: feat  fix  docs  style  refactor  perf  test  chore  ci
```

Examples:
```bash
git commit -m "feat(agents): add git-keeper agent"
git commit -m "fix(topology): update chopsticks remote"
git commit -m "chore: update typescript to 5.5"
```

Header max 100 characters. No sentence-case, PascalCase, or UPPER_CASE in the description.

---

## Branches

Use the type as your branch prefix:

```bash
git checkout -b feat/short-description
git checkout -b fix/short-description
git checkout -b docs/short-description
```

---

## PR Workflow

Canonical standard:

https://github.com/madebymadhouse/bot-dev-playbook/blob/main/AGENTIC_GIT_WORKFLOW.md

Default rule: agents push branches and open PRs; humans review and merge.

---

## Getting Help

- Open an issue in the relevant repo
- Open a discussion or issue in the relevant repo
