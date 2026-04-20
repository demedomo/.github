# Security Policy

## Supported Versions

Security patches are maintained for the current version of each active project.

| Project | Supported |
|---------|-----------|
| madebymadhouse/agents | ✅ |
| madebymadhouse/bot-dev-playbook | ✅ |
| madebymadhouse/vps-maintenance-playbook | ✅ |
| madebymadhouse/chopsticks-lean | ✅ |
| madebymadhouse/chopsticks | ✅ |
| madebymadhouse/liquibar | ✅ |

---

## Reporting a Vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Report privately:

1. **GitHub Security Advisory** (preferred) — use the "Report a vulnerability" button on the affected repo's Security tab
2. **Private Maintainer Contact** — use repository maintainers for private coordination if advisory creation is not available

Include:
- A clear description of the vulnerability
- Steps to reproduce
- Potential impact
- Any suggested mitigations

---

## What to Expect

- Acknowledgement within 48 hours
- Fix targeted within 14 days for critical issues
- Credit in the changelog unless you prefer to stay anonymous

---

## Scope

In-scope:
- Authentication and authorization bypasses
- Remote code execution
- Data exposure (user data, API keys, tokens)
- XSS in web-facing surfaces
- CSRF vulnerabilities
- Injection attacks (SQL, command, etc.)
- Secrets committed to git history

Out of scope:
- Self-hosted deployments with misconfigured secrets
- Social engineering
- Physical attacks
- Issues in third-party dependencies already publicly disclosed (report upstream)

---

## Responsible Disclosure

We follow a coordinated disclosure model. Please give us reasonable time to fix before publishing details publicly.
