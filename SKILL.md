---
name: diagonal-progress-planning
description: Coordinate staged implementation planning across multiple completion targets by establishing cross-target result dependencies and a revisable coarse order, projecting diagonal progress, and updating only affected plans.
---

# Diagonal Progress Planning

Use this skill when planning or revising staged implementation progress across multiple separately identifiable completion targets.

Use each target's owning workflow to define its completion boundary, local implementation plans, and completion criteria.
Use ordinary `plan-driven-planning` for plan boundaries, dependency semantics, authoritative records, durable states, and concurrency constraints.
This skill coordinates results across targets without redefining those responsibilities.

## Start from available results

Read the established and planned results, direct dependencies, and relevant completion targets from the repository's current planning state.
Include the targets currently relevant to the requested work; extend the analysis as other targets become relevant.
Use target-local planning to create or refine independently establishable and verifiable partial results.
Proceed with unrelated supported results while other targets still need local planning.

## Relate results across targets

Compare the partial results that may be needed by more than one target.
When another target needs a prerequisite, record a direct dependency on the specific result that supplies it, rather than requiring completion of its entire target.
Keep independently establishable producing results separate; attach combination dependencies to the first result that actually requires the combination.
Treat implementation scope and result dependencies separately.
Use isolated test setup as evidence of a result's independent validity, not as the definition of repository-level dependencies.

When targets require the same established responsibility or behavior, identify one authoritative producing result and let the other targets reference it.
Base reuse on settled requirements, design, current repository behavior, or confirmed plan boundaries.
A shared helper, file, type, or module alone does not establish a result dependency.
Keep production and target membership in the owning local workflow; a result can serve multiple targets without gaining multiple authoritative owners.

Record confirmed direct dependencies using the ordinary planning index convention.
When the needed boundary cannot be represented because a local plan combines independently establishable results, return that target to local planning for decomposition.
Return invalid local dependencies or unresolved requirements to their owning workflow while keeping unaffected targets available.

## Establish diagonal progress

Derive a coarse, revisable implementation order from confirmed prerequisites.
Identify targets that can start independently, targets whose first useful result becomes viable later, and results that must wait for prerequisites.
Introduce another target when its first useful result is viable; completion of an earlier target is not a prerequisite unless a specific required result establishes that dependency.
Keep independent viable branches unordered.
When multiple valid orders remain, prefer progress that establishes useful target behavior sooner; favor lighter additional work where grounded effort and complexity support the distinction.
Keep tied or uncertain alternatives at the same priority.

Project only the partial results needed to guide the work currently being planned.
As a projected result becomes available in the planning scenario, reassess affected targets and dependencies.
Treat projection as revisable planning guidance, not as a completed plan state or a committed execution schedule.

## Revise affected work

Start revisions from the repository's established planning state.
Trace a changed result or dependency through the planned work that actually depends on it.
Revise the affected cross-target dependencies, coarse order, and progress projections until they are consistent again, preserving unrelated established decisions and independent branches.
Return changes to target-local plan boundaries and completion conditions to their owning workflow.
Use the ordinary plan-driven replanning rules when an implementation attempt has invalidated a plan boundary.

## Record and hand off

Keep confirmed direct dependencies distinct from preferred order and projected milestones.
Record coarse order in an appropriate existing Markdown planning document; no special file format or independently mutable progress status is required.
Leave plan-level concurrency conflicts to ordinary implementation planning.
When a workflow uses synchronized waves, leave exact wave assignment, wave fixing, and execution eligibility to its wave-planning rules.
This cross-target analysis is not a gate for arranging unrelated eligible work.

This skill owns cross-target result coordination, coarse diagonal order, incremental projection, and affected-progress revision.
Target-local decomposition, target completion and testing rules, synchronized wave placement, execution, and implementation review belong to their respective workflows.
