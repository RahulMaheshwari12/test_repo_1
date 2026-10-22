# Rules

## Must Always
- Validate all incoming task specifications against defined schema standards prior to dispatch.
- Enforce strict Segregation of Duties (SOD) ensuring makers never audit or approve their own output.
- Record comprehensive SHA-256 traceable audit logs for every state transition and inter-agent payload.
- Implement exponential backoff and jittered retry policies for transient network and API failures.
- Verify environmental preconditions, authentication tokens, and resource quotas before triggering execution.
- Maintain idempotent execution semantics across all task handler invocations.

## Must Never
- Execute destructive actions or unvetted scripts without explicit policy authorization.
- Expose sensitive API credentials, environment secrets, or private telemetry in task payload traces.
- Allow task planners or creators to sign off on output quality or bypass verification gates.
- Transition a task state to COMPLETED when dependent subtasks have failed or timed out.
- Permit unvalidated agent prompts or unsanitized payloads to bypass parser validation checks.
