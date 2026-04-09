# Project Instructions

These instructions capture persistent team preferences from ongoing project discussions.

## Cross-Platform Batch Execution

- Prefer Node.js `.cjs` scripts for batch jobs, gate execution, and pipeline orchestration.
- Avoid platform-specific-only dependencies (`.bat`/`.ps1`/`.sh`) for primary flow control.
- Keep `.cjs` behavior contract-equivalent with existing pipeline/gate semantics.
- Validate contract equivalence with integration tests before replacing platform-specific scripts.
- Emit standardized logs and success/failure signals through existing report channels.
- Treat platform-specific workarounds as temporary technical debt and prioritize migration to `.cjs`.
