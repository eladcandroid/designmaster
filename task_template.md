# Engineering Task Template

This template defines the required structure for implementing engineering tasks.

Agents must follow this workflow **after task routing and context resolution**.

Execution must align with:

- `task_router.md`
- `context_resolver.md`
- `workflow_engine.md`

---

# 0. Task Routing (Pre-Step)

Before using this template, the task must be classified using:

- `task_router.md`

The router determines:

- task type
- complexity
- required execution depth

---

# 1. Task Summary

Provide a short summary of the requested change.

Include:

- the feature, bug, or refactor requested
- the expected outcome

Example:

Add retry logic to the API client to handle transient network failures.

---

# 2. Affected Components

Identify the parts of the repository that may be involved.

Examples:

- modules
- services
- utilities
- tests
- configuration

List specific files when possible.

---

# 3. Current Behavior

Describe how the system behaves today.

Explain:

- how the current code works
- where the limitation or bug exists

This ensures the change is based on the real implementation.

---

# 4. Root Cause (for bugs)

If the task is a bug fix, explain the root cause.

Examples:

- missing validation
- incorrect error handling
- invalid assumptions about inputs

Avoid speculative explanations.

---

# 5. Implementation Plan

Describe the minimal set of changes required.

The plan should include:

- files to modify
- functions to update
- new utilities if required
- test updates

Large architectural changes should be avoided unless required.

Planning must align with:

- `change_planning.md`
- system constraints defined in `system_contract.md`

---

# 6. Safety Checks

Confirm the change will not break:

- public APIs
- CLI commands
- configuration behavior
- backward compatibility

If such changes are necessary, they must be explicitly noted.

Safety must align with:

- `guardrails.md`
- `system_contract.md`

---

# 7. Implementation

Apply the planned code changes.

Follow:

- repository architecture guidelines
- code style guidelines
- minimal diff principle

Implementation must respect:

- `workflow_engine.md` execution rules
- `context_resolver.md` decisions

---

# 8. Validation & Metrics

All outputs must be validated before completion using:

- `validation_agent.md`
- `metrics.md`

Requirements:

- validation must pass
- quality thresholds must be met

If validation fails:

- corrections must be applied before continuing

---

# 9. Testing

Verify the change using:

- existing test suites
- extended tests for edge cases

Tests should confirm:

- expected behavior
- failure scenarios when applicable

---

# 10. Verification

After implementation:

- run all tests
- confirm no regressions occur
- confirm the original problem is resolved

---

# 11. Change Summary

Provide a concise summary of the final change.

Include:

- files modified
- key logic changes
- new tests added

---

## Design Requirements (MANDATORY)

Before implementation, define:

- Layout Strategy (from design_variation_engine.md)
- Visual Tone
- Typography Style
- Interaction Level
- Density

These must form a unique combination.

Generic layouts are not allowed.

The task is incomplete if design decisions are not explicitly defined before implementation.

---

# Execution Note

This template defines **task structure**, not execution order.

Execution order is enforced by:

- `workflow_engine.md`

All tasks must pass through:

- routing → context → execution → validation → metrics

before being considered complete.