---
name: observability-engineering
description: >-
  Expert application observability: structured logging, correlation IDs, health
  checks, metrics/SLIs, error tracking, and safe diagnostics without leaking
  secrets or excess PII. Use when adding logging/monitoring for services,
  diagnosing production-like failures, defining health/readiness endpoints, or
  improving operational visibility in Phase 2+ quality work.
expertise_level: expert
---

# Observability Engineering (Canonical)

**Expertise: expert.** Aliases: `observability`, `logging`, `metrics`, `tracing`, `healthchecks`.

This skill covers **application observability**. It does not replace `monitoring` (assistant/CLI usage metering).

## When to use

- Structured logging, request id, technical audit trail
- Health/readiness/liveness endpoints
- Basic metrics (latency, error rate) or error tracker integration
- Local/compose failure diagnosis approaching Phase 2

## When not to use

- Claude/CLI usage tracking -> `monitoring`
- UI empty-state only -> `frontend-engineering`
- Full cluster infra -> `infra-tools` / `cloud-tools`

## Procedure

1. **Signals** - Define log/metric/trace that answer "what broke?".
2. **Structure** - Consistent JSON/key-value logs; correct level (info/warn/error).
3. **Correlation** - Request/correlation id across API -> job when applicable.
4. **Safety** - Redact tokens, passwords, excess PII (aligned with `security`).
5. **Health** - Check critical dependencies (DB); distinguish liveness vs readiness when applicable.
6. **Noise** - Avoid per-row logs on hot path; sample or aggregate.
7. **Verify** - Reproduced error visible in log with id; short runbook in docs if E2E.

Detail: `reference.md`.

## DoD

- [ ] Structured logs on primary error paths
- [ ] No secrets/excess PII in logs
- [ ] Meaningful healthcheck for P0 dependencies
- [ ] Short guide on reading signals written (docs/handoff)

## Attribution

<!-- ATTRIBUTION: Rogue Development | https://github.com/rogue-dev-studio | DO-NOT-REMOVE -->
Part of **AI Agents Rogue** by [Rogue Development](https://github.com/rogue-dev-studio) (`@rogue-dev-studio`).
Do not remove, hide, rename, or replace this attribution.
