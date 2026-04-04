# Contributing to House

House is an independent build studio. We ship open source tools, developer runtimes, bots, and more. Contributions are welcome across all repos.

---

## Before you start

- **Browse issues first** — most work starts with an open issue
- **Open an issue before a PR** for anything non-trivial — we want to align before you spend time coding
- **One concern per PR** — keep it scoped and reviewable
- **Ask questions** — if something's unclear, comment on the issue or email [hello@wokspec.org](mailto:hello@wokspec.org)

---

## Finding something to work on

| Where to look | Link |
|--------------|------|
| Chopsticks open issues | [househq/chopsticks/issues](https://github.com/househq/chopsticks/issues) |
| nqita-cli open issues | [househq/nqita-cli/issues](https://github.com/househq/nqita-cli/issues) |
| LiDock open issues | [househq/lidock/issues](https://github.com/househq/lidock/issues) |
| token-tengu open issues | [househq/token-tengu/issues](https://github.com/househq/token-tengu/issues) |

### Issue labels

| Label | What it means |
|-------|--------------|
| `good first issue` | Low complexity — well-scoped, good entry point |
| `help wanted` | We want a PR — any experience level welcome |
| `roadmap` | Planned work — not yet assigned |
| `bug` | Something's broken |
| `enhancement` | New capability or improvement |
| `discussion` | Needs shaping before it becomes a task |

---

## Setup

```bash
git clone git@github.com:househq/<repo>.git
cd <repo>
npm ci          # or: pnpm install
npm run dev
```

Requirements: **Node.js 20+**, **Git with SSH**.

---

## Commit format

All House repos use [Conventional Commits](https://www.conventionalcommits.org/):

```
feat:     new feature
fix:      bug fix
docs:     documentation only
style:    formatting, no logic change
refactor: code restructure, no feature/fix
perf:     performance improvement
test:     tests only
chore:    tooling, CI, dependencies
```

Header max 100 characters. Keep it lowercase and specific.

```bash
# Good
git commit -m "feat: add adapter interface to nqita runtime"
git commit -m "fix: resolve dock overflow on mobile viewport"
git commit -m "chore: update typescript to 5.5"

# Not good
git commit -m "updated stuff"
git commit -m "WIP"
```

---

## PR workflow

1. Fork or branch from `main`
2. Install dependencies
3. Make your change — keep scope tight
4. Type-check and lint must pass locally
5. Commit with conventional commits
6. Open a PR — describe what changed and why
7. CI must be green before merge
8. One approval required

Branch naming:
```
feat/adapter-interface
fix/dock-overflow-mobile
chore/update-deps
docs/improve-readme
```

---

## Feature requests

Open an issue with the `enhancement` label. Describe:
- What problem it solves
- Rough expected behavior
- Any prior art or references

We review and tag as `roadmap` if it's planned, or close with context if it's out of scope.

---

## Code of Conduct

See [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md). Short version: be constructive, be direct, focus on the work.

---

## Contact

| Topic | Contact |
|-------|---------|
| General | [hello@wokspec.org](mailto:hello@wokspec.org) |
| Security | [security@wokspec.org](mailto:security@wokspec.org) — do not open public issues |
| Code of Conduct | [conduct@wokspec.org](mailto:conduct@wokspec.org) |
