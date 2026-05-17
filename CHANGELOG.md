# Changelog

The skill records its compilation date here. The regulatory currency check protocol reads this file at runtime to determine what window of updates to search for.

## v1.0.0 · 2026-05-17

**Compilation date:** 17 May 2026.

**Regulatory snapshot at compilation:**
- AIFMD II (Directive (EU) 2024/927) is in force since 16 April 2026. Phased RTS implementation: liquidity management tools and enhanced Annex IV reporting RTS deferred to 16 April 2027.
- CSSF Circular 25/901 (19 December 2025) in effect for SIFs, SICARs, Part II UCIs.
- ESMA Guidelines on liquidity management tools of UCITS and open-ended AIFs (ESMA34-671404336-1364) published March 2026.
- Luxembourg transposition: Bill of Law 8628, Memorial A on 9 March 2026, effective 16 April 2026, no gold-plating.
- ILPA Principles 3.0 (2019) and ILPA Model LPA WOF Version (July 2020) are the latest published.
- SFDR Level 1 in force; Level 2 RTS (Delegated Regulation 2022/1288) in force.
- ELTIF 2.0 (Regulation (EU) 2023/606) in force since 10 January 2024.

**Known pending items at compilation date (re-check at runtime):**
- ESMA final RTS on open-ended loan-originating AIFs (was draft when this skill was compiled).
- CSSF FAQs updating implementation guidance on AIFMD II Annex IV reporting (expected H2 2026).
- ESMA Q&A on delegation FTE tracking (expected over the course of 2026).
- ILPA guidance refresh on NAV facilities and GP-led secondaries (rolling).
- ILPA Model LPA potential 4.0 refresh (no announced date).

## Update protocol

This skill should be updated whenever any of the sources in `references/regulatory_sources_to_monitor.md` publishes a material change. To update:

1. Add a new version entry above this one with the new compilation date.
2. Capture the new regulatory snapshot.
3. Update the affected reference files (`checklist_aifmd_ii.md`, `checklist_ilpa.md`, `checklist_luxembourg.md`, `emerging_topics.md`) with the new content.
4. Re-run the test suite in `test/` and any new test cases added since the last version.
5. Commit and re-publish.

When the skill version is older than 6 months at runtime, the regulatory currency check will instruct the model to be especially aggressive about searching for updates.
