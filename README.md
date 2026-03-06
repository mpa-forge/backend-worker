# backend-worker

Go background worker repository for the platform blueprint.

## Structure
- `cmd/`: worker entrypoints
- `internal/`: private worker application code
- `pkg/`: shareable public packages
- `deploy/`: deployment manifests and charts
- `docs/`: worker-specific documentation
- `scripts/`: local utility and developer scripts

## Toolchain
- Go `1.24.12`
- Version pin source: `.tool-versions` and `go.mod`

## Setup
Run one of the following bootstrap commands from the repository root:
- PowerShell: `./scripts/bootstrap.ps1`
- POSIX shell: `./scripts/bootstrap.sh`

Bootstrap validates the pinned Go toolchain and runs `go mod download`.
If `mise` or `asdf` is available, the script will use it to install the pinned toolchain automatically.

## Run
No runnable worker entrypoint exists yet.
Worker bootstrap and local run commands will be added in later Phase 1 tasks.

## Test
No automated test suite is configured yet.
Linting, formatting, and test commands will be introduced in `P1-T04` and later tasks.
