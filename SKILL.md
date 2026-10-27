---
name: diagonal-progress-planning
description: Arrange and revise staged implementation progress for one or more completion targets using partial-result prerequisites, cross-target coordination when needed, and incremental projections.
---

# Diagonal Progress Planning

Use this skill when arranging or revising staged implementation progress for one or more completion targets.

Use each target's owning workflow to define its completion boundary, local implementation plans, and completion criteria.
Use `plan-driven-planning` for plan boundaries, direct-dependency semantics, authoritative records, durable states, and concurrency constraints.
This skill coordinates the progression of partial results without redefining those responsibilities.

## Start from available results

Read established results from current settled requirements/design and verified behavior on the relevant base branch; read pending results, direct dependencies, and completion targets from the repository's current planning state. Use completed plans as historical evidence when needed.
Use target-local planning to create or refine independently establishable and verifiable partial results.
Plan from the results currently supported by settled requirements and existing work; extend the projection as further results become relevant.
Progress within one target does not require other targets to be planned. Continue arranging unrelated supported work while another target still needs local planning.

## Relate prerequisite results

For each relevant partial result, use established direct dependencies to identify which preceding results it requires.
Keep independently establishable producing results separate; attach a combination dependency to the first plan result that actually requires the combination.
Treat implementation scope and result dependencies separately.
Use isolated test setup as evidence of a result's independent validity, not as the definition of repository-level dependencies.

When multiple targets are relevant, compare their partial results. Record cross-target direct dependencies on the specific producing plan while its prerequisite result is still pending on the relevant base branch, rather than requiring an entire preceding target to complete.
When targets use the same already-established responsibility or behavior, reference its current requirements/design canon and verified repository baseline. When a shared result is still planned, identify one authoritative producing plan for all dependent targets.
Base reuse on settled requirements, design, current repository behavior, or confirmed plan boundaries.
A shared helper, file, type, or module alone does not establish a result dependency.
Keep the producing plan's ownership and target membership with the owning local workflow; one result may serve several targets.

Record confirmed direct dependencies using the ordinary planning index convention.
If a needed result boundary cannot be represented because a local plan combines independently establishable results, return it to target-local planning for decomposition.
Return invalid local dependencies or unresolved requirements to their owning workflow while keeping unaffected results available.

## Arrange staged progress

Derive a coarse, revisable progression through the partial results of the targets currently in scope.
For a single target, advance its useful partial results as their prerequisites are established or projected.
For multiple targets, identify independently startable targets and introduce another target when its first useful result becomes viable; the earlier target need not complete first.
Interleave viable target steps when doing so makes useful target behavior available sooner.
Preserve independent viable branches as a partial order rather than inventing dependency edges to encode a preferred sequence.

Among supported alternatives, prefer earlier useful progress and lighter incremental work when the available planning information supports a difference.
Compare additional work beyond already established or planned results, and keep tied or uncertain alternatives at the same priority.

Project only the results needed to guide the requested work.
After placing a projected milestone, treat its expected result as available within that planning projection and reassess affected eligible work.
Continue until the requested target or targets are represented by sufficient planned structure.
A projected result is planning guidance, not an established repository result, a completed durable plan state, or an execution commitment.

## Revise affected progress

Start revisions from the repository's established planning state.
Trace a changed result or dependency through the planned results that actually depend on it.
Revise the affected dependencies, coarse order, and progress projections while preserving unaffected plans and independent branches.
Return changes to target-local plan boundaries or completion conditions to their owning workflow.
Use ordinary plan-driven replanning rules when an implementation attempt invalidates a plan boundary.

## Record and hand off

Keep confirmed direct dependencies distinct from preferred order and projected milestones.
Record useful coarse order in an appropriate existing Markdown planning document; no special file format or independently mutable progress status is required.
Leave plan-level concurrency conflicts to ordinary implementation planning.
When synchronized waves are used, wave planning owns exact placement, fixedness, the pre-execution gate, and execution eligibility.
Progress projection does not gate the arrangement of unrelated eligible work.

This skill owns staged progress through partial results for one or more completion targets, cross-target result coordination when needed, incremental projection, and affected-progress revision.
Target-local decomposition, completion and testing rules, synchronized wave placement, execution, and implementation review belong to their respective workflows.
