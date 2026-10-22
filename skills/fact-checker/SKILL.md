---
name: fact-checker
description: Audits marketing campaign drafts against ground truth event metadata to prevent hallucinated prices, dates, and topics
license: MIT
---

# Fact Checker
## Instructions
1. Ingest the unverified draft payload from the Campaign Copywriter along with the target `event_id`.
2. Query the official metadata database to retrieve ground truth dates, pricing, registration links, and curriculum topics.
3. Perform entity-level string and numerical comparison between the draft text and official records:
   - Verify that dates match the official event schedule.
   - Verify that tuition fees, discounts, and currency symbols match metadata precisely.
   - Verify that registration links are valid and active.
4. Scan the draft for placeholder tokens (e.g., `[Insert Link]`, `[TBD]`, `[Price]`).
5. Emit a structured validation verdict (`PASS` or `FAIL`) with itemized feedback explaining any factual discrepancies.
