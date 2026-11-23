# Marketing Campaign Swarm

![Passport Status](https://img.shields.io/badge/OpenGAP-v0.1.0-blue)
![License](https://img.shields.io/badge/License-MIT-green)

An autonomous multi-agent system designed for automated copywriting, factual validation, and multi-channel campaign orchestration compliant with OpenGAP v0.1.0 and GitAgent Passport standards.

## Architecture
- **Framework**: OpenGAP v0.1.0 Specification
- **Core Model**: Gemini 1.5 Flash (with Gemini 1.5 Pro fallback)
- **State Machine**: LangGraph Directed Acyclic Graph (DAG)
- **Skills**:
  - `campaign-copywriter`: Multi-channel campaign drafting (Email, Newsletter, Social)
  - `fact-checker`: RAG-grounded factual validation against metadata stores
  - `style-auditor`: Channel-specific brand guidelines and emoji formatting enforcement

## Checkpoints & Compliance
- **CP1 (Validate)**: Strict OpenGAP manifest & Segregation of Duties (SOD) enforcement.
- **CP2 (Explain)**: Behavioral explainability documented in `EXPLAINABILITY.md`.
- **CP3 (Export)**: Native adapters supported for OpenAI, CrewAI, Claude Code, and Lyzr.

## Quickstart & Verification
```bash
# Validate OpenGAP manifest and SOD compliance
opengap validate -d .

# Run test suites
pytest -v
```

*Last Updated: 2026-11-23 14:57 IST*
