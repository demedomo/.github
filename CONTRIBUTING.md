# Contributing to Mad House

Mad House ships bots, agent tooling, playbooks, runtime experiments, and org-wide GitHub defaults. Contributions are welcome, but the workflow is explicit: branch first, PR second, human merge last.

---

## Before You Start

- **Read the repo first** — don't submit a PR to a repo whose scope you haven't read
- **One concern per PR** — keep it scoped and reviewable
- **Use a branch** — agents and humans work on branches, not on `main`
- **Open a PR with a real body** — What / Why / Testing / Notes

---

## Repos In Scope

| Repo | Link |
|--------------|------|
| Agents | [madebymadhouse/agents](https://github.com/madebymadhouse/agents) |
| Bot Dev Playbook | [madebymadhouse/bot-dev-playbook](https://github.com/madebymadhouse/bot-dev-playbook) |
| VPS Maintenance Playbook | [madebymadhouse/vps-maintenance-playbook](https://github.com/madebymadhouse/vps-maintenance-playbook) |
| Chopsticks Lean | [madebymadhouse/chopsticks-lean](https://github.com/madebymadhouse/chopsticks-lean) |
| Chopsticks | [madebymadhouse/chopsticks](https://github.com/madebymadhouse/chopsticks) |
| Liquibar | [madebymadhouse/liquibar](https://github.com/madebymadhouse/liquibar) |

### Shared Expectations

- Conventional commits
- One logical change per commit
- One PR, one thing
- CODEOWNERS where review responsibility matters
- Shared workflow described in the Bot Dev Playbook

---

## Setup

```bash
git clone git@github.com:househq/<repo>.git
cd <repo>
npm ci          # or: pnpm install
npm run dev
```

Requirements vary by repo. Default toolchain assumptions:
- **Node.js 22+** for bot repos
- **pnpm** for workspace repos like Liquibar
- **GitHub CLI** for PR-first workflow

---

## Workflow Standard

Mad House uses branch-first, PR-first development.

Canonical standard:

https://github.com/madebymadhouse/bot-dev-playbook/blob/main/AGENTIC_GIT_WORKFLOW.md

Short version:
1. Create a branch from `main` or `dev` as documented in that repo
2. Make one scoped change
3. Commit with conventional commits
4. Push the branch
5. Open a PR with What / Why / Testing / Notes
6. Human reviews and merges

---

## Commit Format

All Mad House repos use [Conventional Commits](https://www.conventionalcommits.org/):

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

## PR Workflow

Every PR should answer four things:
1. What changed
2. Why it changed
3. How it was tested
4. Anything the reviewer should watch for

Branch naming:
```
feat/adapter-interface
fix/dock-overflow-mobile
chore/update-deps
docs/improve-readme
```

---

## Code of Conduct

See [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md). Short version: be constructive, be direct, focus on the work.
