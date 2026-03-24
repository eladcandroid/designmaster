# Developer Workflow

This document describes the human development workflow.

All agent execution is governed by:
- agent_workflow.md
- workflow_engine.md

The goal is to combine human engineering judgment with AI-assisted implementation while maintaining architectural discipline and code quality.

---

Step 1 — Define the Task
Step 1 — Define the Task
## Step 1 — Define the Task

The developer begins by defining a task using `task_template.md`.

Tasks should include:

- objective
- affected modules
- constraints
- acceptance criteria

The task template ensures the AI agent receives structured instructions rather than vague prompts.

---

## Step 2 — Agent Loads Context

Before performing any work the agent must read:

AGENTS.md  
model_instructions.md  
instruction_priority.md  
guardrails.md  

These files define behavior, safety rules, and instruction hierarchy.

---

System Awareness
System Awareness
System Awareness
System Awareness
System Awareness
System Awareness
## Step 3 — System Awareness

The agent then loads project context:

architecture.md  
repo_map.md  
environment.md  

This allows the model to understand:

- repository structure
- system architecture
- development environment

---

## Step 4 — Planning Phase

Before writing code the agent must generate a change plan using:

change_planning.md

The plan should describe:

- affected components
- implementation steps
- potential risks

The developer reviews the plan before implementation.

---

## Step 5 — Implementation

The agent writes code while following:

code_style.md  
anti_overengineering.md  

These standards ensure generated code remains readable, maintainable, and minimal.

---

## Step 6 — Debugging

If problems occur, the agent must follow the structured debugging process defined in:

debugging_playbook.md

The debugging workflow emphasizes:

- isolating root causes
- testing incremental changes
- verifying assumptions

---

## Step 7 — Pull Request Preparation

Before submitting work the agent prepares documentation and commits according to:

pr_rules.md

This ensures that human reviewers can easily understand the change.

---

## Human Responsibilities

The developer remains responsible for:

- validating architectural decisions
- approving change plans
- reviewing generated code
- ensuring long-term maintainability

The AI agent acts as a development assistant, not an autonomous decision maker.