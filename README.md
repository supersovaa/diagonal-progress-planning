# diagonal-progress-planning

Arrange staged progress through partial results of one or more completion targets. Multiple targets can advance diagonally without requiring one target to finish before another begins.

## Skill

- [diagonal-progress-planning](SKILL.md) — use when arranging or revising staged implementation progress for one or more completion targets: project useful partial results, coordinate cross-target prerequisites when needed, and update affected progress.

The skill follows the phase separation used by [cell-complete-development](https://github.com/supersovaa/cell-complete-development): local planning defines each target's parts, shared planning guides staged progress and coordinates multiple targets when needed, and wave planning assigns executable batches when used.

## Responsibilities

- [plan-driven-planning](https://github.com/supersovaa/plan-driven-implementation/blob/main/skills/plan-driven-planning/SKILL.md) owns ordinary implementation-plan boundaries, direct-dependency semantics, persistent state, and concurrency conflicts.
- Target-specific planning owns the completion target, local decomposition, membership, and completion criteria.
- **diagonal-progress-planning** owns staged progress for one or more targets, cross-target result coordination when needed, incremental projection, and affected-progress revision.
- A target workflow's wave-planning skill owns wave assignment, pre-execution gates, and synchronization when waves are used. Diagonal progress does not require waves.
- Target-specific review owns behavioral completion and testing obligations.

A pending implementation result may contribute to several targets while retaining one authoritative producing plan. Established results are referenced through current canon and verified repository behavior; completed results awaiting integration carry an integration prerequisite instead. Preferred order is guidance; only pending implementation results establish direct plan dependencies.

## Installation

Install this repository's `SKILL.md` as the `diagonal-progress-planning` skill using your agent's skill loader.
Also install `plan-driven-planning` and the target-specific planning skills required for your workflow.
For Cell workflows use `cell-planning`, add `cross-planning` when coordinating multiple Cells, and use `wave-planning` for wave assignment. A single Cell can be wave-planned without cross planning.
For user-facing use cases use `use-case-driven-planning`; `use-case-driven-review` remains responsible for use-case behavior evidence.
