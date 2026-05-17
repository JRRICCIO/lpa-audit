# Grading · LPA Audit test · Iteration 1

Grading the test output at `test_output_iteration_1.md` against the answer key in `test_lpa_snippet.md`.

---

## Per-expected-finding scorecard

| # | Expected finding | Expected severity | My audit | Caught? |
|---|---|---|---|---|
| 1 | Hurdle / Preferred Return: simple interest, not compounding | AMBER | Finding 8, AMBER, explicit redline to compound annually | **YES** |
| 2 | Management Fee: no step-down at end of investment period | AMBER | Finding 9, AMBER, redline with step-down to invested capital basis | **YES** |
| 3 | GP Commitment: GP-determined amount, fee waiver or borrowed funding | RED | Finding 10, RED, redline imposing 2% cash, no waiver/borrowing | **YES** |
| 4 | Key Person: trigger lacks dedication-of-time, LPAC-discretionary suspension, no cure period | AMBER-to-RED | Finding 11, RED, hits all three sub-issues with redline | **YES** |
| 5 | Liquidity Management Tools: only suspension, AIFMD II requires at least two | RED | Finding 3, RED, redline adding gates + notice + suspension | **YES** |
| 6 | Indemnification: fraud-only carveout, missing gross negligence et al. | RED | Finding 14, RED, redline with full carveout list, plus Luxembourg public-policy enforceability point on faute lourde / dol | **YES** |
| 7 | LPAC: advisory only, no consent rights | RED | Finding 12, RED, full redline with consent matters list, plus composition fix | **YES** |
| 8 | Conflicts: GP sole discretion, no LPAC consent | RED | Finding 5, RED, redline imposing LPAC consent on affiliate transactions | **YES** |
| 9 | Side Letters: no MFN, no disclosure | RED | Finding 15, RED, redline with disclosure schedule and tiered MFN election | **YES** |
| 10 | Removal of GP: 95% + non-appealable court judgment = impossible | RED | Finding 13, RED, redline with majority for-cause + 75% no-fault | **YES** |
| 11 | Loan Origination: no 5% retention, no concentration, no credit policy review | RED | Finding 2, RED, redline with retention, concentration cap, policy review, no originate-to-distribute | **YES** |
| 12 | Silences on AIFM, leverage, delegation, reporting, default, transfer, recycling, valuation, clawback (each silence on a mandatory item = RED) | RED | AIFM and delegation in Finding 4 (RED), leverage in Finding 1 (RED), reporting in Finding 6 (RED), default/transfer/recycling in Finding 18 (RED), valuation in E1 (RED), clawback in E2 (RED), SCSp Law 2013 silences in Finding 16 (RED), information rights in Finding 17 (RED), change of control of GP in E3 (AMBER) | **YES** (compound finding; all major silences flagged; minor LP-list / LPAC in-camera / LP communication-rights items folded into Finding 12 redline but not separately enumerated — **PARTIAL** on those three sub-items) |

**Score:** 11 out of 12 fully caught; 1 partial (the silence compound item — captured 10 of the ~13 silences flagged in the answer key, with 3 minor sub-items (LP list separately, LPAC in-camera rights as a standalone finding, LP communication rights as a separate clause) folded into the LPAC redline rather than enumerated as standalone findings).

**Effective catch rate: 11.5 / 12 = 96%.**

---

## False positives in my audit

- **Sustainability (Finding 7, AMBER).** Not on the answer key. Arguably defensible because the prompt names it as one of the 18 areas (7. Sustainability — SFDR Art 8/9 classification consistency). Reporting AMBER for SFDR silence is consistent with prompt instructions ("Treat silence on a mandatory item as RED"); I downgraded to AMBER on the grounds that Article 6 default classification is permissible. Borderline; not strictly a false positive because the prompt requires reporting on all 18 areas.
- No other findings outside the answer key's scope. Emerging topics (valuation, clawback, change of control of GP) all map to item 12's silence list, so they are not false positives.

---

## Severity calibration

**Over-severity (called RED where AMBER expected):** None. Items 1, 2 were AMBER expected and called AMBER. Items expected RED were called RED.

**Under-severity (called AMBER where RED expected):** None on the answer key items. Sustainability (Finding 7) was called AMBER but is not on the answer key, so no calibration error there.

**Edge case:** Key Person was tagged "AMBER-to-RED" by the answer key. My audit went RED. Defensible because all three sub-issues compound (no dedication-of-time prong + LPAC discretion + no cure period + no termination mechanism), but if the prompt intended to leave RED for the most severe cases, AMBER would have been the conservative call. I lean to RED here being correct given the cumulative defect.

---

## What I caught beyond the answer key

- Luxembourg-specific public policy point on faute lourde / dol unenforceability in indemnification (Finding 14). This is a real Luxembourg counsel point and strengthens the indemnification redline.
- AIFM identity silence flagged as part of the delegation finding (Finding 4) and called out in the executive summary "What to fix" — consistent with prompt instruction ("If the LPA does not name the AIFM, flag the silence and ask in the executive summary").
- Recycling cap with both percentage cap and time window in the redline.
- Change of control of GP as emerging topic (E3).
- Valuation methodology as emerging topic (E1), with AIFMD II Article 19 hook.

---

## Top 3 things to improve in the prompt

1. **Enumerate the silence-checklist more explicitly.** The answer key item 12 lists ~13 distinct silences (AIFM identity, leverage cap and method, delegation, reporting cadence, default mechanics, transfer regime, recycling, valuation methodology, fiduciary duty clarification, LP communication rights, change of GP control consent, LPAC in-camera rights, LP list, clawback). My audit hit the big ones but folded LPAC in-camera and LP list / LP communication rights into other findings rather than as separate items. The prompt should instruct: "Produce a separate 'Silences' subsection at the end of Section C that enumerates every silence-on-mandatory-item finding as a bullet list, even if the topic is also addressed elsewhere." This would prevent compaction of multiple silences into a single redline.

2. **Make the emerging-topics output mandatory and named.** The prompt currently asks for "the 18 areas plus any emerging topics," but does not specify where to put them, what severity defaults apply, or which emerging topics to look for (valuation, clawback, change of GP control, GP-led secondaries, ELTIF 2.0 read-across, ESG SFDR Article 6 vs 8 vs 9 stating, fund-of-one vs commingled mechanics, US parallel vehicle considerations). Naming a short emerging-topic checklist would prevent the LLM from omitting valuation or clawback when the document is silent.

3. **Tighten the AMBER-to-RED bridge for compound defects.** The prompt's severity rubric is binary per finding, but real defects often compound (e.g., key person has three sub-defects, each AMBER alone but RED in combination). Add: "Where a single area has two or more sub-defects each of which would be AMBER alone, escalate to RED and list the sub-defects in the Issue paragraph." This would standardise the call I made on Key Person and prevent under-severity on compound governance failures.

---

## Iteration 1 summary

- **11 of 12 fully caught, 1 partial (sub-items of the compound silence finding). Catch rate ~96%.**
- **No false positives** (Sustainability AMBER is defensible per prompt).
- **No under-severity** on answer-key items. **No over-severity** on answer-key items.
- **Top 2 prompt changes recommended:** (1) require an enumerated "Silences" subsection so every silence-on-mandatory-item is listed separately; (2) name a short emerging-topics checklist (valuation, clawback, change of GP control, etc.) to ensure consistent coverage when the document is silent.
