# Architecture Guidelines

This repository follows a **clarity-first architecture philosophy**.

Code must remain understandable to engineers who did not originally write it.

---

## Core Principles

1. Prefer simple architectures over complex ones.
2. Prefer composition over inheritance.
3. Prefer explicit behavior over implicit behavior.
4. Prefer small modules with clear responsibilities.

## System Architecture Layers

In addition to code-level architecture, the system operates across defined execution layers.

```plaintext
1. Input Layer
   - task_router.md

2. Context Layer
   - context_resolver.md
   - state_manager.md

3. Execution Layer
   - workflow_engine.md
   - agents

4. Validation Layer
   - validation_agent.md
   - metrics.md

5. Optimization Layer
   - prompt_optimizer.md

6. Recovery Layer
   - failure_handler.md

7. Governance Layer
   - system_contract.md
   - guardrails.md
```

These layers ensure that the system is:

- predictable
- enforceable
- scalable

## Separation of Concerns

When designing systems, maintain clear boundaries between:

### Domain Logic

- Pure business logic
- Independent from infrastructure
- Easily testable in isolation

### Infrastructure

External systems such as:

- databases
- APIs
- file systems
- message queues
- external services

Infrastructure must not contain business logic.

### Interfaces

Entry points into the system such as:

- HTTP handlers
- CLI commands
- UI components
- background jobs

Interfaces should coordinate work but avoid embedding domain logic.

## Module Structure

Modules should:

- have a single responsibility
- expose minimal public interfaces
- avoid circular dependencies

Prefer multiple small modules over large monolithic files.

## File Size Guidelines

Files should generally remain under approximately `500` lines.

If a file grows beyond this size, consider splitting it into focused modules.

Large files reduce maintainability and increase cognitive load.

## Function Complexity

Functions should remain small and focused.

- Prefer functions that perform a single logical task.
- Avoid functions exceeding approximately `50` lines unless necessary.
- Large functions should be broken into smaller composable units.

## Dependency Direction

Dependencies should flow inward toward domain logic.

- Infrastructure should depend on domain logic.
- Domain logic must never depend directly on infrastructure.

## State Management

Avoid hidden state.

Prefer:

- explicit inputs
- explicit outputs
- immutable data where practical

State handling must align with:

- `state_manager.md` for persistence and lifecycle
- `context_resolver.md` for context prioritization

Implicit state creates unpredictable behavior and difficult debugging.

## Error Handling Architecture

Error handling must be explicit and consistent.

Failures must be handled through:

- `failure_handler.md` for classification and recovery
- `debugging_playbook.md` for root cause resolution

Prefer returning structured errors rather than relying on implicit failure modes.

Do not swallow errors.

Failures should:

- propagate clearly
- include useful diagnostic context
- remain observable during debugging

## Public Interface Stability

Public interfaces should remain stable.

Avoid breaking API contracts unless explicitly requested.

This includes:

- CLI commands
- HTTP endpoints
- exported modules
- public library APIs

Backward compatibility must be preserved whenever possible.

## Testing Relationship

Domain logic must be easily testable.

Design systems so that business logic can be tested without:

- databases
- external services
- network access

Prefer dependency injection or interface boundaries when required.

## Complexity Control

Avoid introducing:

- unnecessary abstraction layers
- speculative architecture
- framework-heavy patterns

Architecture must serve the problem, not impress the reader.

## Refactoring Expectations

Refactoring is allowed when it improves:

- clarity
- maintainability
- safety

Refactoring must not change behavior unless explicitly required.

## Execution Alignment

All architecture must support:

- `workflow_engine.md` for enforced execution order
- `task_router.md` for correct task classification
- `validation_agent.md` for correctness verification
- `metrics.md` for measurable quality

Architecture is not only structural; it must support system execution and reliability.

## Final Principle

The system includes a Design Layer responsible for enforcing visual differentiation and identity.

Good architecture is not just clean code.

It is a system that behaves:

- consistently
- predictably
- correctly under pressure
