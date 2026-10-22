---
name: campaign-copywriter
description: Drafts channel-specific marketing copy across Email, Newsletter, and Social Media based on verified syllabus RAG context
license: MIT
---

# Campaign Copywriter
## Instructions
1. Retrieve semantic syllabus chunks and official event metadata for the target `event_id`.
2. Determine audience persona calibration (Students, Working Professionals, or Executive Leaders).
3. Draft content tailored to the designated channel:
   - **Email**: Create subject line, preview text, body paragraphs, and single high-visibility CTA with zero emojis.
   - **Social Media**: Compose high-impact opening hook, core value points, relevant hashtags, and maximum 3 emojis.
   - **Newsletter**: Formulate comprehensive curriculum breakdown, instructor bio spotlight, and full pricing breakdown.
4. Output the structured draft payload and pass to the Fact Auditor for verification.
