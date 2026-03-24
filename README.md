# Designmaster

A structured AI development framework for Claude Code that enforces disciplined engineering workflows with validation, recovery, and quality metrics.

Adapted from [codexmaster](https://github.com/robbiecalvin/codexmaster) by robbiecalvin.

## Install

```bash
npx skills add eladcandroid/designmaster
```

## What It Does

Transforms Claude from an ad-hoc assistant into a reliable engineering agent. Every task is:

- **Routed** — classified by type and complexity
- **Executed** — through a defined workflow pipeline
- **Validated** — for correctness and completeness
- **Measured** — against quality thresholds (0-12 scoring)
- **Recovered** — with structured failure handling

### Pipeline

```
Route > Resolve > Execute > Validate > Measure > Improve > Recover
```

## Core Components

### Governance
- `system_contract.md` — guarantees and boundaries
- `guardrails.md` — hard safety rules
- `instruction_priority.md` — conflict resolution hierarchy

### Input & Context
- `task_router.md` — task classification and workflow selection
- `context_resolver.md` — authoritative context resolution
- `state_manager.md` — state tracking

### Execution
- `workflow_engine.md` — enforced execution order
- `agent_workflow.md` — agent execution model
- `change_planning.md` — pre-edit planning protocol
- `task_template.md` — task structure

### Validation & Metrics
- `validation_agent.md` — correctness verification
- `metrics.md` — quality scoring (accuracy, completeness, clarity, efficiency, reliability, compliance)

### Recovery
- `failure_handler.md` — failure classification and recovery
- `debugging_playbook.md` — root cause analysis

### Engineering Standards
- `architecture.md` — composition, separation of concerns
- `code_style.md` — readability and conventions
- `anti_overengineering.md` — simplicity rules
- `security_playbook.md` — input validation, threat awareness

### Design System (UI tasks)
- `design_system.md` — anti-generic design rules
- `design_memory.md` — pattern reinforcement
- `design_variation_engine.md` — layout diversity

## License

MIT
