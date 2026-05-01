# Contributing to openmcphub

Thanks for considering a contribution. This document captures the org-wide conventions. Each repo may add its own `CONTRIBUTING.md` with module-specific details on top of these.

---

## Branching strategy — GitFlow

```
main           → tagged releases only (production)
develop        → integration branch (default for PRs)
feature/<n>-*  → new features (branch from develop)
fix/<n>-*      → bug fixes (branch from develop)
hotfix/<n>-*   → critical production fixes (branch from main)
```

**Always branch from `develop`, not `main`.** Branch name format: `<type>/<issue-number>-<slug>`. Example: `feature/12-add-twitter-provider`.

---

## Commit convention — Conventional Commits

```
<type>(<scope>): <short description>
```

**Types:** `feat`, `fix`, `docs`, `test`, `refactor`, `style`, `chore`, `ci`.

The scope is repo-specific — see each repo's `CONTRIBUTING.md` for the canonical scope list. When in doubt, look at recent commits.

**Examples:**

```
feat(domain): add WHOIS fallback for .io tld
fix(npm): handle 429 rate-limit response
docs(adr): add ADR-0005 on rate-limit strategy
chore(infra): bump fastmcp to 2.3.0
```

---

## Test-driven development

TDD is the default workflow:

1. Write the test first (or extend an existing one).
2. Watch it fail.
3. Make the smallest change that makes it pass.
4. Refactor.

V0 stub providers return `NOT_IMPLEMENTED` and the test asserts that contract. Real implementations land in subsequent phases backed by mocked HTTP responses (we use `respx` in Python, equivalent fakes in other stacks).

CI runs the test suite, the linter, and the type checker on every PR. PRs that fail any of those three are blocked.

---

## Pull request process

1. Open a PR against `develop` (never `main`).
2. Fill out the PR template — don't skip the checklist.
3. Mark it as a draft if it's not ready for review.
4. Run the local equivalents of CI (`pytest`, `ruff check`, `ruff format --check`, `mypy src` for Python repos) before pushing.
5. One approval required from `@wileverg` for now. As the org grows we'll move to per-repo CODEOWNERS.
6. Squash-merge preferred. The squash commit message must follow Conventional Commits.

---

## Filing issues

Use the issue templates from the **New Issue** menu:

| Template | When to pick it |
|---|---|
| Bug report | Something is broken or behaves unexpectedly |
| Feature request | Proposing new behavior or a new MCP tool |
| Provider request | Asking for a new external provider integration |

Avoid the blank issue option unless none of the templates fits.

---

## License of contributions

By contributing to a repo, you agree your contribution is licensed under that repo's declared license:

- Most repos: **Apache-2.0**.
- `brand-check`: **AGPL-3.0** (deliberate copyleft choice to defend against fork-and-host capture; see ADR-0002 in that repo).

There is no separate CLA at this stage.

---

## Security

Do **not** open public issues for vulnerabilities. Use the GitHub Private Security Advisory form on the affected repo, or email the maintainer at `wilevergomez@gmail.com`. See [SECURITY.md](./SECURITY.md).

---

## Maintainer

[@wileverg](https://github.com/wileverg). Reach out via issues or `wilevergomez@gmail.com` for anything that doesn't fit a public thread.
