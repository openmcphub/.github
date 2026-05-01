# Security policy

Thanks for helping keep `openmcphub` users safe.

---

## Supported versions

`openmcphub` repos are pre-1.0. Security fixes target `develop` and the most recent tagged release of the affected repo. There are no LTS branches yet.

| Repo | Latest tagged | Status |
|---|---|---|
| [`brand-check`](https://github.com/openmcphub/brand-check) | `v0.0.0-alpha.1` (planned) | Pre-release |
| [`bench`](https://github.com/openmcphub/bench) | none | Phase 0 |

---

## Reporting a vulnerability

**Do not open a public GitHub issue for vulnerabilities.**

Two reporting channels:

1. **GitHub Private Security Advisory** (preferred) — open one on the affected repo via the Security tab. This is the right path for repo-specific issues.
2. **Email** — `wilevergomez@gmail.com` with subject line `[openmcphub] Security report — <repo>`. Use this for org-level concerns or if the issue spans multiple repos.

Future channel (not yet active): `security@openmcphub.org` once the domain is registered.

---

## What to include

- Affected repo and version (commit hash if running from main/develop).
- Steps to reproduce, with the smallest possible repro case.
- Impact: what does an attacker gain — data leak, RCE, DoS, cache poisoning, exfiltrated tokens?
- Whether you are publishing or have published a CVE.

---

## What you can expect from us

- **Acknowledgement** within 72 hours.
- **Triage decision** (accepted / not a vuln / duplicate) within 7 days.
- **Fix and disclosure plan** within 30 days for critical issues, 90 days for non-critical.
- Public credit on the disclosure unless you ask to remain anonymous.

We will not pursue legal action against good-faith researchers who follow this policy.

---

## What is in scope

- Code in any `openmcphub/*` repo.
- Provider integrations: how we call upstream services, how we cache responses, how we surface errors.
- Build and CI tooling that is part of a published release.

---

## What is out of scope

- Vulnerabilities in upstream dependencies — please report those upstream. We will pick up the fix once the upstream patches.
- Issues only reproducible against a fork or against a hosted Pro tier (when one exists).
- Social engineering of maintainers or users.
- DoS via traffic floods to upstream provider APIs we depend on.

---

## Disclosure

We follow coordinated disclosure. Once a fix lands and a patched release is tagged, we publish a security advisory on the repo with credit to the reporter (unless requested otherwise) and a CVE if one was assigned.
