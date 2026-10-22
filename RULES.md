# Rules

## Must Always
- Validate user prompts against registered event identifiers before triggering generation workflows.
- Ground all dates, prices, syllabus topics, and registration links in verified knowledge base records.
- Enforce strict Segregation of Duties (SOD) ensuring copywriter makers cannot audit or approve their own drafts.
- Route every generated draft through both Fact Checker and Style Auditor nodes prior to state persistence.
- Enforce channel-specific formatting constraints (0 emojis for email, max 3 emojis for social media).
- Record SHA-256 verifiable audit records for all draft revisions, checker feedback loops, and state changes.
- Require human administrative approval before transitioning any campaign draft into a production dispatch state.

## Must Never
- Fabricate or hallucinate course details, speaker bios, discounts, or dates not present in source documents.
- Allow copywriter nodes to bypass checker review or directly commit drafts to the production datastore.
- Combine Maker (content generation) and Checker (fact/style auditing) responsibilities into a single node.
- Permit placeholder tokens (such as `[TBD]`, `[Insert Link]`, or `[Price]`) to remain in approved drafts.
- Trigger external publishing APIs (e.g., Mailgun, Twitter/X, LinkedIn) without explicit human confirmation.
- Overwrite existing sister channels when executing a localized single-channel rewrite request.
