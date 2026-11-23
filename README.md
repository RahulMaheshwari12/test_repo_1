# Marketing Campaign Swarm

An autonomous multi-agent system designed for automated copywriting, factual validation, and multi-channel campaign orchestration compliant with OpenGAP v0.1.0 and GitAgent Passport standards.

## Architecture
- **Framework**: OpenGAP v0.1.0 Specification
- **Core Model**: Gemini 1.5 Flash (with Gemini 1.5 Pro fallback)
- **Skills**:
  - `campaign-copywriter`: Multi-channel campaign drafting (Email, Newsletter, Social)
  - `fact-checker`: RAG-grounded factual validation against metadata stores
  - `style-auditor`: Channel-specific brand guidelines and emoji formatting enforcement

## Checkpoints & Compliance
- **CP1 (Validate)**: Strict OpenGAP manifest & Segregation of Duties (SOD) enforcement.
- **CP2 (Explain)**: Behavioral explainability documented in `EXPLAINABILITY.md`.
- **CP3 (Export)**: Native adapters supported for OpenAI, CrewAI, Claude Code, and Lyzr.

*Last Updated: 2026-11-23*
