# Security Policy (org-wide, applies to all hakodb repositories
without their own SECURITY.md)

## Reporting a vulnerability

Do NOT open a public issue. Email the maintainer address listed on
the repository's main page, or open a
[private vulnerability report](../../security/advisories/new)
(Security tab → Advisories) on the affected repository.

Include: affected repo + version/tag, impact, and reproduction steps
or proof of concept. Reports in Indonesian or English are both fine.

## What to expect

- Acknowledgement within 7 days.
- Fix or mitigation plan communicated before any public disclosure.
- Credit in the release notes if you want it (or anonymity — your call).

## Scope notes

- Secrets accidentally committed: rotate first, then report (push
  protection blocks most of these at commit time).
- Test/demo credentials and local-only findings are out of scope.
- Automated scanner output without demonstrated impact is low priority.
