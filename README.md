# diagonal-progress-planning

Plan staged progress across multiple separately identifiable completion targets without requiring one target to finish before another begins.

## Skill

- [diagonal-progress-planning](SKILL.md) — use when planning or revising cross-target implementation progress: relate partial results, establish direct cross-target dependencies, choose a revisable coarse diagonal order, and update affected projections.

The skill follows the phase separation used by [cell-complete-development](https://github.com/supersovaa/cell-complete-development): local planning defines each target's parts, cross-target planning coordinates them, and optional wave planning assigns executable batches.

## Responsibilities

- [plan-driven-planning](https://github.com/supersovaa/plan-driven-implementation/blob/main/skills/plan-driven-planning/SKILL.md) owns ordinary implementation-plan boundaries, direct-dependency semantics, persistent state, and concurrency conflicts.
- Target-specific planning owns the completion target, local decomposition, membership, and completion criteria.
- **diagonal-progress-planning** owns cross-target result coordination, coarse order, incremental projection, and affected-progress revision.
- A target workflow's wave-planning skill owns wave assignment, pre-execution gates, and synchronization when waves are used. Diagonal progress does not require waves.
- Target-specific review owns behavioral completion and testing obligations.

A planned result may contribute to several targets while retaining one authoritative producer. Preferred order is guidance; only actual result prerequisites establish direct dependencies.

## Installation

Install this repository's `SKILL.md` as the `diagonal-progress-planning` skill using your agent's skill loader.
Also install `plan-driven-planning` and the target-specific planning skills required for your workflow.
For Cell workflows use the accompanying `cell-planning` and `cross-planning` skills, with `wave-planning` when arranging waves.
For user-facing use cases use `use-case-driven-planning`; `use-case-driven-review` remains responsible for use-case behavior evidence.
