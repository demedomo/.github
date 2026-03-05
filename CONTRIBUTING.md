# Contributing to WokSpec

Thanks for wanting to contribute. WokSpec is a collection of AI-native products and tools built for creators. We welcome bug fixes, features, improvements, and documentation.

---

## Quick Reference

| Repo | What it is | License |
|------|------------|---------|
| [WokTool](https://github.com/WokSpec/WokTool) | 80+ browser dev/design tools | MIT |
| [Chopsticks](https://github.com/WokSpec/Chopsticks) | Discord bot | MIT |
| [Eral](https://github.com/WokSpec/Eral) | AI layer — API, extension, widget | FSL-1.1-MIT |
| [Dilu](https://github.com/WokSpec/Dilu) | No-code product builder | FSL-1.1-MIT |
| [Vecto](https://github.com/WokSpec/Vecto) | AI design studio | FSL-1.1-MIT |
| [WokGen](https://github.com/WokSpec/WokGen) | AI pixel art generation | Apache-2.0 |
| [WokPost](https://github.com/WokSpec/wokpost) | AI-curated news | FSL-1.1-MIT |
| [WokAPI](https://github.com/WokSpec/WokAPI) | Auth and product registry | FSL-1.1-MIT |

---

## Commits

WokSpec uses **Conventional Commits**:

```
feat:     new feature
fix:      bug fix
docs:     documentation only
style:    formatting, no logic change
refactor: refactor (no feature/fix)
perf:     performance improvement
test:     tests
chore:    tooling, CI, deps
```

Examples:
```
feat: add CSV export to json-tools
fix: resolve CORS header on /v1/chat route
chore: update dependabot config
docs: improve CLAUDE.md with auth patterns
```

---

## Workflow

1. **Fork** the repo or create a branch if you have write access
2. **Install** dependencies (`npm ci` in most repos)
3. **Write** your change — keep it focused and minimal
4. **Typecheck**: `npx tsc --noEmit`
5. **Lint** (if ESLint is configured): `npx eslint . --max-warnings 0`
6. **Test** (if tests exist): check the repo's `package.json` scripts
7. **Commit** using conventional commits
8. **Push** and open a pull request

---

## Pull Requests

- Fill in the PR template fully
- Link the issue you're solving (if any)
- Keep the diff small and focused — one concern per PR
- Passing CI is required before merge

---

## Issues

- Bug? Use the Bug Report template
- Feature? Use the Feature Request template — labeling it `sweep` enables [Sweep AI](https://sweep.dev) to attempt an automated implementation

---

## AI Agents

WokSpec repos include `CLAUDE.md` and `.coderabbit.yaml` to give AI agents full context. If you're using Claude Code, GitHub Copilot, Cursor, or similar tools:

- Read `CLAUDE.md` first — it contains the critical constraints for each repo
- Follow the commit conventions above
- Run typecheck before committing
- Don't modify auto-generated files (`prisma/migrations/`, `.next/`, `out/`, etc.)

---

## Security

Found a vulnerability? See [SECURITY.md](SECURITY.md) — please don't open a public issue.

---

## Code of Conduct

Be respectful. See [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
