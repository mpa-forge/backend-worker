# Agent Context

## Local Entry Point

This file is the repo-local entry point for agent context.

## Always Load

Before making changes:

1. Read `README.md`.
2. Read `Makefile` if present.
3. Run `make sync-agent-skills` before starting major changes or when shared skill guidance may have changed.
4. Read `../platform-blueprint-specs/common/AGENTS.md`.
5. Read `.codex/skills/automated-ai-worker/SKILL.md` when the repo is being changed by an automated AI worker or when following the same autonomous workflow manually.
6. Read `../platform-blueprint-specs/implementation/phases/phase-2-contracts-service-skeletons-and-data-baseline.md`.
7. Read `../platform-blueprint-specs/implementation/phase-tasks/phase-2-contracts-service-skeletons-and-data-baseline-tasks.md`.
8. Check local repo docs under `docs/` if the task touches worker runtime details.

## Repo Role

- Own the product background worker runtime, separate from the AI automation worker.
- Start with a pluggable async adapter and no queue technology locked in yet.

## Relevant Shared Constraints

- Queue strategy remains deferred until product requirements justify it.
- Worker should still have a clean runtime skeleton, health surface, structured logs, and startup config validation.
- Shared backend observability library will be introduced so API and worker use one telemetry contract.

## Consult Conditionally

- `../platform-blueprint-specs/platform-specification.md` only when the task needs broader platform architecture or deployment decisions.

## Shared Managed Skills

Run `make sync-agent-skills` before major changes so the local common skill
copies stay current.

## Typical Validation

- `make lint`
- `make test`
- `make format-check`

## Priority of Instructions

Repo-local instructions override shared planning docs.

If local repo docs conflict with a shared planning file, the more specific repo or task instruction wins.
