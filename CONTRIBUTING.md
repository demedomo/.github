# Contributing to WokSpec

WokSpec is at an early stage — we're building Web3 and AI infrastructure and actively looking for people to grow with. Whether you're a developer, designer, artist, or researcher, there's a place here.

---

## What We're Building

| Product | What it is | Status |
|---------|------------|--------|
| **Orinadus** | Web3 research & intelligence platform — on-chain analysis, DeFi research, AI Authors | Active |
| **Autiladus** | Client services — sites, systems, automations. Small team, fast delivery | Active |
| **NQITA** | AI companion with OS-level overlay — moods, memory, persistent presence | Private beta |
| **WokStudio** | Internal tooling and infrastructure | Internal |
| **WokAPI** | Auth, billing, product registry | Internal |

---

## Open Positions / Roles We Need

We're early-stage and filling roles across the board. If any of these fit, reach out.

**Design & Art**
- UI/UX designer — particularly for Web3 dashboards and data-heavy interfaces
- Pixel artist / illustrator — for NQITA character art, game assets, and brand visuals
- Motion designer — micro-animations, loading states, identity work

**Frontend**
- Next.js / React developer comfortable with Tailwind and component systems
- Web3 frontend — wagmi, viem, wallet connection, on-chain data rendering

**Backend / Infrastructure**
- Cloudflare Workers developer (Hono, D1, R2, Queues)
- Blockchain data engineer — indexing, event streaming, subgraphs (The Graph / Ponder)
- Solidity / smart contract developer

**Research & Content**
- Web3 researcher for Orinadus — DeFi protocols, on-chain analysis
- Technical writer — documentation, whitepapers, protocol explainers

---

## How to Get Involved

1. **Reach out directly** — [hello@wokspec.org](mailto:hello@wokspec.org). Tell us what you do, what you're interested in, and link relevant work.
2. **Look at open issues** — public repos have labeled issues. `good first issue` and `help wanted` are the entry points.
3. **Propose something** — if you see a gap or have an idea, open an issue first before submitting a PR.

---

## Commit Style

We use [Conventional Commits](https://www.conventionalcommits.org/):

```
feat:     new feature
fix:      bug fix
docs:     documentation only
style:    formatting, no logic change
refactor: no feature/fix, just structure
perf:     performance
test:     tests only
chore:    tooling, CI, deps
```

---

## Pull Request Workflow

1. Fork or branch (if you have write access)
2. `npm ci` to install
3. `npx tsc --noEmit` — must pass
4. `npx eslint . --max-warnings 0` — must pass
5. Commit with conventional commits
6. Open PR — small and focused, one concern per PR
7. CI must be green before merge

---

## Code of Conduct

See [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md).

---

## AI Agents

All repos include a `CLAUDE.md` with constraints and context for AI-assisted development. If you're using Claude Code, Cursor, or similar — read it first.
