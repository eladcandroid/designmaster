# Codex Master

A structured Codex system combined with a Website Blueprint Generator to produce consistent, non-generic AI-generated websites.

## The Problem

AI-generated websites tend to:
- reuse the same layouts
- ignore design intent
- produce inconsistent results across runs

## The Solution

Codex Master solves this with two systems:

### 1. Execution System (Codex Master)
Enforces structured workflows, validation, and consistency.

### 2. Blueprint Generator
Forces design diversity by generating varied, non-repetitive website structures before execution.

Result:
- consistent builds
- non-generic design
- repeatable outcomes


## Overview

This system turns Codex from a free-form assistant into a structured engineering agent.

Every task is:
- routed
- executed through a defined workflow
- validated for correctness
- measured for quality
- improved through feedback


## System Pipeline

Route → Resolve → Execute → Validate → Measure → Improve → Recover

A closed-loop system that prevents drift, enforces correctness, and continuously improves output quality.

---

Each layer is modular and can be used independently or as part of the full system.

## Core Components

### Governance Layer
Defines rules, priorities, and system boundaries.

- `guardrails.md`
- `instruction_priority.md`
- `model_instructions.md`
- `system_contract.md`

---

### Input & Context Layer
Determines task classification and relevant context.

- `task_router.md`
- `context_resolver.md`
- `state_manager.md`

---

### Execution Layer
Controls how tasks are performed.

- `workflow_engine.md`
- `agent_workflow.md`
- `task_template.md`
- `change_planning.md`

---

### Validation Layer
Ensures correctness and completeness.

- `validation_agent.md`
- `metrics.md`

---

### Recovery Layer
Handles failures and system resilience.

- `failure_handler.md`
- `debugging_playbook.md`

---

### Optimization Layer
Improves performance over time.

- `prompt_optimizer.md`

---

### Engineering Standards
Maintains code quality and consistency.

- `architecture.md`
- `code_style.md`
- `anti_overengineering.md`
- `repo_map.md`
- `environment.md`

---

## Key Properties

### Deterministic Execution
Tasks follow structured workflows instead of ad-hoc reasoning.

### Context Awareness
Conflicting inputs are resolved using defined priority rules.

### Reliability
Outputs are validated and measured before acceptance.

### Continuous Improvement
Failures and metrics drive system refinement.

### Scalability
Modular components allow extension without breaking behavior.

---

## Execution Flow

All tasks follow this sequence:

1. **Task Routing**  
   Classify task type and complexity (`task_router.md`)

2. **Context Resolution**  
   Determine authoritative context (`context_resolver.md`, `state_manager.md`)

3. **Execution**  
   Run through enforced workflow (`workflow_engine.md`)

4. **Validation**  
   Verify correctness (`validation_agent.md`)

5. **Metrics Evaluation**  
   Measure quality (`metrics.md`)

6. **Failure Handling (if needed)**  
   Classify and recover (`failure_handler.md`)

7. **Optimization (if needed)**  
   Improve prompt structure (`prompt_optimizer.md`)

---

## Role of the Agent

The agent operates as a structured engineering assistant.

It must:

- follow defined workflows
- respect instruction hierarchy
- produce minimal, correct changes
- avoid unnecessary complexity
- validate all outputs before completion

The agent does not operate through free-form reasoning.

All actions are governed by system rules and execution flow.

---

## Role of the Developer

Human developers remain responsible for:

- architectural decisions
- system design
- reviewing outputs
- evolving the framework

The system is designed to assist, not replace, engineering judgment.

---

## Principles

- correctness over speed
- clarity over cleverness
- minimal changes over large rewrites
- explicit behavior over implicit assumptions

---

## Getting Started

1. Define a task using `task_template.md`
2. Ensure routing via `task_router.md`
3. Follow execution through `workflow_engine.md`
4. Validate and measure results
5. Refine if necessary

---

## Final Note

This is not a prompt collection.

It is a controlled AI development environment designed to produce reliable, repeatable, and maintainable engineering outcomes.
