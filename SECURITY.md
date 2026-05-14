# Security Policy

## Supported Versions

| Version | Supported |
|---|---|
| v1.x.x | Yes |

## Reporting a Vulnerability

Do **not** open a public issue for security vulnerabilities.

Instead, report them privately via [GitHub's private vulnerability reporting](https://github.com/Joydeep2005Banik/readme-stats-cards/security/advisories/new).

Include:
- A description of the vulnerability
- Steps to reproduce it
- The potential impact

You will receive a response within 72 hours. If the issue is confirmed, a fix will be released and credited to you in the changelog unless you prefer to remain anonymous.

## Token Security

This action accepts a `token` input. Always pass it via `${{ secrets.GITHUB_TOKEN }}` or a repository secret — never hardcode a token value directly in your workflow file.

The minimum required scopes are:
- Public stats only: `GITHUB_TOKEN` is sufficient
- Private repository stats: PAT with `repo` and `read:user` scopes