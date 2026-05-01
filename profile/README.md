# openmcphub

> Open source MCP servers for the modern dev.

We build provider-agnostic, well-tested MCP servers and release them under permissive open-source licenses, so devs and small teams can plug them into Claude, Cursor, Continue, or any MCP-aware client without vendor lock-in.

---

## Why this exists

Several incumbents in the MCP ecosystem are closed-source, paywalled behind tiers most indie builders can't justify, or coupled to a single LLM provider. Some are great products. None of them are a community-owned commons.

`openmcphub` exists to be that commons — the open-source alternative for the dev-tools surface that LLM agents actually need.

---

## Active modules

| Repo | What it does | Status |
|---|---|---|
| [`brand-check`](https://github.com/openmcphub/brand-check) | Brand availability across domains, code registries, social handles, trademarks, LLC names. Successor to Brandomica. | V0 in development |
| [`bench`](https://github.com/openmcphub/bench) | Provider-agnostic LLM benchmark MCP — local LLMs first (Ollama, LM Studio), online providers next, community leaderboard later. | Phase 0 (bootstrap) |

Future planned modules: compliance gates, ISO 25000 / ISO 27000 audit scaffolding, and other dev-tooling MCPs the community pulls toward.

---

## Roadmap (next 3–6 months)

- **2026 Q2** — Ship `brand-check` V0 (4 providers + cache + tests) and `bench` V0 (local LLMs).
- **2026 Q3** — `brand-check` V1 (social handles + scoring), `bench` V1 (online providers + reproducibility seal).
- **2026 Q4** — Community leaderboard for `bench` with hardware fingerprinting; first compliance MCP scaffolding.

The roadmap moves with contributor pull, not internal pressure. If a use case is loud, it ships earlier.

---

## How to contribute

Each repo has its own `CONTRIBUTING.md`, but the org-wide conventions are:

- **GitFlow** — branch from `develop`, PR against `develop`, tag releases on `main`.
- **Conventional Commits** — `feat(scope): …`, `fix(scope): …`, etc.
- **TDD** — every PR ships with tests. Stub providers return `NOT_IMPLEMENTED` until covered by a test.
- **License** — new repos default to **Apache-2.0** unless a stronger copyleft (AGPL-3.0) is needed against fork-and-host commercial capture (see `brand-check`'s ADR-0002).

Pick an issue from any active repo, drop a comment that you're picking it up, and open a draft PR early — we'd rather give feedback on shape than on a finished PR you have to redo.

---

## Sponsoring

The hub is a labor of love — provider quotas, hosted demo infra, and maintainer time aren't free.

- **GitHub Sponsors:** enrollment in progress; once active, [github.com/sponsors/openmcphub](https://github.com/sponsors/openmcphub) will be the canonical link.
- **Open Collective:** considered for the moment a corporate sponsor lands. Until then, individual sponsorship via GitHub is the simplest path.

If you ship something built on an `openmcphub` MCP and it saves you a paid tool fee, consider matching that fee as a one-time sponsorship.

---

## Conduct

We follow the [Contributor Covenant 2.1](./CODE_OF_CONDUCT.md). Be kind. Be patient. Assume good faith. The reporting contact is `wilevergomez@gmail.com`.

---

## Security

Vulnerabilities go through GitHub Private Security Advisories on the affected repo, or to `wilevergomez@gmail.com`. See [SECURITY.md](./SECURITY.md) for the full policy.

---

## Maintainer

[@wileverg](https://github.com/wileverg) ([Flowui LLC](https://github.com/wileverg/flowui-technology)).

`openmcphub` started as one founder's portfolio of MCP work spun out into a public collective. The intent is for it to outgrow that origin — if that means handing over the keys, that's a feature, not a bug.
