---
name: agent-coordinator
description: Coordinates agent assignments, monitors execution state, and manages communication handoffs
license: MIT
---

# Agent Coordinator
## Instructions
1. Poll the ready task queue for items whose dependency preconditions have been fully satisfied.
2. Query the agent registry to identify active, non-saturated worker agents with matching capability tags.
3. Construct authenticated task dispatch envelopes containing input schemas, environment context, and timeout constraints.
4. Transmit execution payloads to the designated agent instance and transition the task state to `RUNNING`.
5. Maintain a heartbeat listener on the agent telemetry stream to detect stalled workers or process timeouts.
6. Upon receiving a response payload, route the artifacts to the Execution Auditor for validation and log the transaction hash.
