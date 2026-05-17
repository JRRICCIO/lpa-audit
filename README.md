# Ikhor LPA Audit

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](./CHANGELOG.md) [![Compiled](https://img.shields.io/badge/compiled-2026--05--17-informational)](./CHANGELOG.md) [![Test pass rate](https://img.shields.io/badge/test%20pass%20rate-96%25-brightgreen)](./test/test_grading_iteration_1.md)

A comprehensive first-pass audit framework for Luxembourg SCSp / ASLP Limited Partnership Agreements. Built by Ikhor and shared openly.

## What this is

A structured AI prompt and supporting reference materials that take an LPA from "180 pages of dense legal text" to "an executive summary plus 18 line-item findings with severity ratings, clause citations, and paste-ready redlines" in about 4 minutes of model time.

The package covers AIFMD II (in force 16 April 2026), CSSF Circular 25/901, ILPA Principles 3.0, and Luxembourg fund formation law.

## Why we built this

We do this review every week internally. The first pass used to take a junior associate 90 minutes of locate-and-summarise work before a senior could engage. With this prompt, the locate-and-summarise is automatic. Senior time goes to judgement, not lookup.

We are releasing it because the bottleneck on Luxembourg fund formation is no longer information; it is execution speed. Faster first passes, better LPs, fewer surprises at closing.

## Regulatory currency

The skill compiles its rule base on a specific date (see `CHANGELOG.md`). Regulation moves. When the skill runs, it performs a regulatory currency check: if web tools are available, it searches ESMA, CSSF, EBA, ILPA, and Legilux for material updates since the compilation date and incorporates any new parameters. If web tools are not available, it declares the cutoff date in the report and recommends manual re-check before close.

This means a user running the prompt six months after compilation gets a report that reflects the regulation at the time of running, not at the time of compilation, provided the LLM has web access. The full source list is in `references/regulatory_sources_to_monitor.md`.

## How to use it

### Option A. Use as a Claude Skill

If you have Claude Skills enabled in Claude.ai or Claude Code, drop this entire folder into your skills directory. The skill will trigger on prompts like "review my LPA", "audit our limited partnership agreement", "is this AIFMD II compliant".

### Option B. Use the standalone prompt

Open `prompt_standalone.md`. Copy the entire prompt section. Paste it into Claude (Opus or Sonnet) or any modern LLM. When the model is ready, paste your LPA into the same chat.

This works without Claude Skills, in any LLM client. The output quality is highest on Claude Opus 4.6, then Claude Sonnet 4.6, then GPT-5, in our internal testing.

### Option C. Have Ikhor run it on your file

The full 18-point version, with senior fund-formation review and remediation drafts, is what we run on real LPAs in 24 hours. Reach us:

- LinkedIn: send a DM to https://www.linkedin.com/company/109984825/
- WhatsApp: +352 661 228 679

## What's in the package

```
ikhor-lpa-audit/
├── SKILL.md                                 The skill definition (for Claude Skills)
├── prompt_standalone.md                     The copy-paste prompt
├── README.md                                This file
├── CHANGELOG.md                             Skill version + regulatory snapshot at compilation
├── references/
│   ├── checklist_aifmd_ii.md                Areas 1-7: AIFMD II regulatory compliance
│   ├── checklist_ilpa.md                    Areas 8-15: ILPA Principles 3.0 alignment
│   ├── checklist_luxembourg.md              Areas 16-18: SCSp / ASLP specifics
│   ├── emerging_topics.md                   E1-E7: subscription lines, continuations, ESG, ELTIF, tax
│   ├── severity_rubric.md                   RED / AMBER / GREEN calibration with examples
│   └── regulatory_sources_to_monitor.md     URLs and update types for the currency check
├── assets/
│   └── example_findings.md                  Two worked examples (one RED, one AMBER)
└── test/
    ├── test_lpa_snippet.md                  Synthetic LPA with 12 known issues for self-test
    ├── test_output_iteration_1.md           Output of the audit on the synthetic LPA
    └── test_grading_iteration_1.md          Grading: 96% catch rate, 0 false positives
```

## What it covers, what it does not

**Covers:**
- AIFMD II compliance (Directive (EU) 2024/927, including phased RTS to April 2027)
- CSSF Circular 25/901 framework for SIFs, SICARs, Part II UCIs
- ILPA Principles 3.0 market standards
- Luxembourg Law of 1915 and Law of 2013 for SCSp / ASLP
- Common drafting conventions and red flags

**Does not cover:**
- US securities law, ERISA, non-EU regulation
- Tax structuring beyond LPA-stated terms
- AML operational procedures
- Pre-marketing rules
- ELTIF 2.0 alignment for ELTIF-eligible vehicles (separate review)
- A complete legal opinion

## Calibration

The skill is calibrated for SCSp / ASLP vehicles. For RAIF, Part II UCI, SICAR, SICAV-RAIF, SIF, the regulatory and market context shifts. The skill will flag this and produce a partial report; for the full version on those vehicles, use the dedicated reviews we maintain internally.

## Licence

Released by Ikhor for the Luxembourg private markets community. Use freely, modify freely, share freely. Attribution appreciated, not required. No warranty: this is a first-pass triage tool, not legal advice.

## Credits

Built by Ikhor. Calibrated against:
- AIFMD II (Directive (EU) 2024/927) and ESMA technical standards
- CSSF Circular 25/901 (19 December 2025) and CSSF FAQs on AIFMD
- ILPA Principles 3.0 (2019) and ILPA Model LPA (Whole-of-Fund and Deal-by-Deal versions)
- Public guidance from Loyens & Loeff, Linklaters, Clifford Chance, Arthur Cox, Dechert, CMS, Ogier, Maples, Elvinger Hoss, KPMG Luxembourg, Trustmoore, and others

For corrections, improvements, or contributions, contact Ikhor via the channels above.
