# State Manager & Context Persistence System

## Purpose

This document defines how the system tracks, updates, compresses, and recalls state across interactions to ensure continuity, accuracy, and operational consistency.

---

## Core Principles

1. State is explicit, not assumed.
2. State must be compressed regularly to avoid drift.
3. Only relevant state is persisted.
4. Every interaction either reads, updates, or validates state.

State is short-term and session-scoped.

Persistent knowledge must be stored in:
- system_memory.md

## State Categories

### 1. System State

- Active modes (Architect, Critic, Builder, etc.)
- Active constraints and guardrails
- Current framework configuration

### 2. Project State

- Current objective
- Active files and components
- Progress stage (planning, building, testing, refining)

### 3. Interaction State

- Last completed step
- Pending actions
- Known ambiguities or unresolved items

## State Lifecycle

### 1. Initialization

At the start of a task:

- Identify project scope
- Load relevant project context
- Activate required modes

### 2. Update Rules

After every meaningful interaction:

- Update progress
- Remove resolved items
- Flag new risks or ambiguities

### 3. Compression

When state becomes large or noisy:

- Summarize into structured bullets
- Remove redundant details
- Preserve only actionable context

### 4. Validation

Before executing major outputs:

- Confirm current state is accurate
- Check for missing dependencies
- Verify alignment with user intent

### 5. Memory Integration

If information is reusable across sessions:

- store in system_memory.md
- do not retain in state

## State Format

State must be stored in structured format:

```plaintext
[STATE]

Project:
- Goal:
- Stage:
- Active Components:

Progress:
- Completed:
- In Progress:
- Next Step:

Risks:
- Known Issues:
- Ambiguities:
```

## Rules for Persistence

- Do not carry irrelevant historical context forward.
- Do not assume continuity without confirmation.
- Always prioritize clarity over completeness.

## Failure Modes

If state is unclear:

- Pause execution
- Request clarification, or
- Reconstruct state explicitly before proceeding

## Integration Points

- Works with: `task_template`, `agent_workflow`, `ChangePlanner`
- Must be referenced before major outputs
- Must be updated after every completed task

## Versioning

State logic must evolve with:

- Framework updates
- New agent integrations
- Increased system complexity
