# Partner

An expert-driven knowledge and workflow framework for AI-assisted delivery.

This repository provides:

- A structured expert system (REASONING modules) for software and enterprise delivery decisions.
- Prompt templates for repeatable planning and review workflows.
- Documentation governance rules to keep planning and decision artifacts consistent.
- Instruction baselines for agent behavior, response style, and execution principles.

## Why This Repository Exists

The goal is to reduce uncertainty quickly and move work forward with clear, auditable decisions.

Instead of generic responses, the workflow encourages:

- Intent-based expert selection.
- Explicit trade-offs and boundaries.
- Requirement-to-implementation traceability.
- Concise, decision-ready outputs.

## Core Concepts

### 1. Expert Reasoning Modules

The expert map is defined in `.partner/reasonings.md` and points to focused modules under `.partner/reasonings/**/REASONING.md`.

Domains:

- `software_development_life_cycle` (13 experts)
- `enterprise_delivery_life_cycle` (16 experts)
- `cross` (1 expert: cross-domain translation)

Typical expert topics include:

- Requirement boundaries and acceptance criteria
- Complexity and trade-off analysis
- Architecture and API contracts
- Testing and integration validation
- Risk/governance reporting
- Change management and delivery quality

### 2. Prompt-Driven Workflow

Prompt templates in `.partner/prompts/` standardize common interactions:

- `docs-plan`: Create a complete plan document in `docs/`
- `plan-review`: Run a structured plan review (depth + anti-overdesign checks)
- `plan-next`: Decide the most valuable next work items
- `do-this`: Execute a recommended item with experts
- `do-all`: Execute all recommended items with experts
- `experts`: Append expert invocation to any request

### 3. Documentation Governance

Governance rules are defined in `docs/governance.md`.

Highlights:

- Clear document categories: active, specs, decisions, archive, drafts
- Sync matrix based on impact scope
- Archive triggers and traceability expectations
- Mandatory AI reading order for consistent retrieval

### 4. Agent Behavior Baseline

`AGENTS.md` and `.partner/instructions/` define persistent behavior, including:

- Resolve highest uncertainty first
- Keep responses compact and action-oriented
- Consult relevant experts for major decisions
- Default discussion/status language is Traditional Chinese, and users can change this preference in `AGENTS.md` or `.partner/instructions/partner-instructions.md`
- Apply TDD principles for code changes (docs/config-only changes are exempt)

## Repository Structure

```text
.
|- AGENTS.md
|- LICENSE
|- README.md
|- docs/
|  |- governance.md
|  |- drafts/
|  |  |- discuss.txt
|  |- template/
|     |- template-plan.md
|- .partner/
	|- instructions/
	|- prompts/
	|- reasonings.md
	|- reasonings/
```

## How To Use

1. Start with your objective (for example: create or review a plan).
2. Use one of the prompt templates in `.partner/prompts/`.
3. Load only relevant experts from `.partner/reasonings.md`.
4. Produce outputs with explicit decisions, trade-offs, and next actions.
5. Update docs according to `docs/governance.md` synchronization rules.

## Planning Template

Use `docs/template/template-plan.md` when creating a new plan file.

The template includes:

- Scope and non-scope
- Revision history
- Expert invocation and conclusions
- Trade-off decisions
- Traceability matrix
- Phased execution plan
- Test strategy, migration/rollback, and risks

## Project Preferences

From `.partner/instructions/project-instructions.md`:

- Prefer Node.js `.cjs` scripts for batch/pipeline orchestration.
- Avoid OS-specific scripts (`.bat`, `.ps1`, `.sh`) as primary control flow.
- Keep behavior contract-equivalent when migrating legacy scripts.

## Current Gaps

The governance document references active files that are not yet present:

- `docs/todo.md`
- `docs/completed.md`
- `docs/roadmap.md`
- `docs/README.md`

Creating these files is a natural next step to make governance fully operational.

## License

MIT. See `LICENSE`.
