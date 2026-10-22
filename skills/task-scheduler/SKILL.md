---
name: task-scheduler
description: Schedules, prioritizes, and resolves dependency graphs for multi-agent task execution
license: MIT
---

# Task Scheduler
## Instructions
1. Ingest incoming workflow definition documents containing job declarations and dependency maps.
2. Build a Directed Acyclic Graph (DAG) validating that no circular dependencies or unresolvable references exist.
3. Compute the topological sorting order to establish the critical execution path and parallel execution tiers.
4. Calculate dynamic priority scores for each task node based on deadline urgency and downstream blocker counts.
5. Push task nodes into the scheduling queue according to priority weights and emit `TASK_SCHEDULED` events to the message broker.
6. Monitor execution feedback; on task completion or failure, update downstream dependency status flags immediately.
