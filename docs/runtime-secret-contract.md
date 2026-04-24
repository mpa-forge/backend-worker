# Worker Runtime Secret Contract (Phase 5 Baseline)

This document captures the secret/config contract for the future
`backend-worker` runtime. It does not claim that runtime wiring is already
implemented in this repository.

## Canonical Secret Source

- Google Secret Manager (GSM) is the canonical runtime secret source.
- Cloud Run delivery reads GSM secrets directly.
- Optional GKE delivery uses External Secrets Operator (ESO) to map the same GSM
  secrets into workload consumption.

## Database Configuration Contract

- `DB_PASSWORD` is the canonical database secret input.
- `DB_HOST`, `DB_NAME`, and `DB_USER` are non-secret runtime configuration.
- `DATABASE_URL` is allowed only as a local development convenience and is not
  the canonical cloud/runtime secret model.

## Repository Configuration Guardrails

- Do not commit plaintext runtime secrets in repository-managed config files.
- Keep `.env.example` values non-sensitive placeholders only.
- Runtime secret identifiers, IAM grants, and delivery wiring are defined in
  `platform-infra`; this repository documents only the worker consumption
  contract for later runtime phases.
