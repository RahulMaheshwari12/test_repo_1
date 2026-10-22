---
name: style-auditor
description: Validates brand voice, layout formatting standards, and channel-specific emoji rules for marketing collateral
license: MIT
---

# Style Auditor
## Instructions
1. Inspect the channel designation of the draft (Email, Social Media, or Newsletter).
2. Count emoji occurrences using Unicode regex patterns:
   - For **Email**: Enforce strictly zero emojis (`count == 0`).
   - For **Social Media**: Enforce maximum 3 emojis (`count <= 3`).
   - For **Newsletter**: Enforce professional header styling and clean typography.
3. Validate presence of mandatory brand elements:
   - Ensure a clear call-to-action is present.
   - Verify proper capitalization, grammar, and paragraph separation.
4. If styling violations exist, return status `FAIL` with specific remediation instructions.
5. If all styling rules pass, return status `PASS`.
