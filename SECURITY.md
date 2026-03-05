# Security Policy

## Supported Versions

WokSpec maintains security patches for the current production deployment of each product. Older versions or self-hosted forks are not covered by this policy.

| Product | Supported |
|---------|-----------|
| WokTool (current) | ✅ |
| Chopsticks (current) | ✅ |
| Eral (current) | ✅ |
| Dilu (current) | ✅ |
| Vecto (current) | ✅ |
| WokGen (current) | ✅ |
| WokPost (current) | ✅ |
| WokAPI (current) | ✅ |

---

## Reporting a Vulnerability

**Please do not open a public GitHub issue for security vulnerabilities.**

Report privately via one of these channels:

1. **GitHub Security Advisory** (preferred): Use the "Report a vulnerability" button on the affected repo's Security tab
2. **Email**: security@wokspec.org

Include:
- A clear description of the vulnerability
- Steps to reproduce
- The potential impact
- Any suggested mitigations

---

## What to Expect

- We'll acknowledge your report within 48 hours
- We aim to ship a fix within 14 days for critical issues
- We'll credit you in the changelog (unless you prefer to stay anonymous)

---

## Scope

In-scope:
- Authentication and authorization bypasses
- Remote code execution
- Data exposure (user data, API keys, tokens)
- Cross-site scripting (XSS) in WokTool or other web apps
- CSRF vulnerabilities
- Injection attacks (SQL, command, etc.)
- Secrets committed to git history

Out of scope:
- Self-hosted deployments with misconfigured secrets
- Social engineering
- Physical attacks
- Issues in third-party dependencies that are already publicly disclosed (report upstream)

---

## Responsible Disclosure

We follow a coordinated disclosure model. Please give us reasonable time to fix the issue before publishing details publicly.
