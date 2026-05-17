# Severity rubric

The severity of a finding is the most important field for the reader. It determines whether the finding goes to the executive summary, whether it blocks closing, and who needs to look at it.

Three levels: RED, AMBER, GREEN. There is no "yellow" or "orange" or "needs attention" category. Force every finding into one of the three.

## RED

A finding is RED when one of the following is true:

1. **Non-compliant with mandatory law or regulation.** Example: an open-ended AIF with no liquidity management tools in the LPA. AIFMD II requires at least two. Silence is non-compliance.

2. **Materially adverse to LP interests vs market standard.** Example: deal-by-deal waterfall with no clawback. ILPA Principles 3.0 treat this as a structural defect, not a deviation.

3. **Creates litigation or regulatory exposure that a reasonable advisor would not let close without fixing.** Example: indemnification of the GP for gross negligence. Even if the LP signs, this is unlikely to hold up in Luxembourg courts and creates avoidable conflict.

4. **Internally inconsistent in a way that breaks the contract.** Example: hurdle rate stated as 8% compounding in one section and 8% simple interest in another. The LPA cannot operate.

RED findings ALWAYS go to the executive summary. RED is "do not close without fixing."

## AMBER

A finding is AMBER when one of the following is true:

1. **Borderline compliance.** Example: leverage cap of 174% on an open-ended LO-AIF. Technically compliant (under 175%) but no margin, and the calculation method might push it over.

2. **Outside market standard but defensible.** Example: 2.25% management fee on committed capital for a first-time fund manager. Above ILPA-typical 2.0%, but a first-time fund with strong differentiated thesis can defend it.

3. **Creates friction.** Example: side letter scope of MFN that excludes "regulatory carveouts" without enumerating them. Workable but leaves room for argument.

4. **Drafting weakness.** Example: a definition that is undefined elsewhere, a cross-reference to a section that does not exist, language that survives but is sloppy.

AMBER findings go to the findings list and only to the executive summary if there are 3 or more or one is particularly stubborn. AMBER is "should fix; if not, document the rationale."

## GREEN

A finding is GREEN when the LPA addresses the area in a way that is compliant, market-standard, and free of obvious drafting issues.

GREEN findings are listed for completeness so the senior reviewer can see what was checked and confirm. Do not write extensive analysis for GREEN findings, just one line confirming the clause exists and is in order.

GREEN does not mean "the GP has been LP-favourable beyond market." It means "no action needed."

## How to calibrate

When you are uncertain between two levels, ask yourself:

- **RED vs AMBER:** Would a reasonable senior associate at a top-tier fund formation firm send the LPA back for revision before close, or annotate the issue on the file and proceed? If revision before close, RED. If annotate and proceed, AMBER.
- **AMBER vs GREEN:** Is there any defensible negotiating ask the LP would make on this clause? If yes, AMBER. If no, GREEN.

## Examples

### Example A. RED finding

**Area:** 14. Standard of care, exculpation, and indemnification.

**Clause:** Section 13.4, page 47.

**Quote:** "The General Partner shall be indemnified by the Fund for any liability arising from the performance of its duties, except in cases of fraud as finally adjudicated by a court of competent jurisdiction."

**Standard:** ILPA Principles 3.0; Luxembourg public policy on indemnification.

**Severity:** RED.

**Issue:** The indemnification carveout is limited to fraud and excludes gross negligence, willful misconduct, material breach of the LPA, and securities law violations. This is materially below market and unlikely to be enforceable for gross negligence under Luxembourg law.

**Suggested redline:** Replace with: "The General Partner shall be indemnified by the Fund for any liability arising from the performance of its duties, except in cases of (i) fraud, (ii) gross negligence, (iii) willful misconduct, (iv) material breach of this Agreement, or (v) violation of applicable securities laws, in each case as finally adjudicated by a court of competent jurisdiction or admitted by the General Partner."

**Owner of fix:** Counsel to GP / LP-side negotiation.

### Example B. AMBER finding

**Area:** 9. Management fee.

**Clause:** Section 6.1, page 22.

**Quote:** "The Management Fee shall be 2.0% per annum of Aggregate Commitments during the Investment Period, and 2.0% per annum of Aggregate Commitments thereafter until the Fund is wound up."

**Standard:** ILPA Principles 3.0 (step-down at end of Investment Period).

**Severity:** AMBER.

**Issue:** Management fee does not step down from the committed-capital basis to an invested-capital basis (or to a lower rate) at the end of the Investment Period. This results in LPs paying management fees on undrawn or returned capital for the entire harvest period, which is outside ILPA standard.

**Suggested redline:** Insert at the end of clause 6.1: "Notwithstanding the foregoing, from and after the expiration of the Investment Period, the Management Fee shall be 1.75% per annum of the Invested Capital then outstanding (excluding capital returned to Limited Partners and capital invested in portfolio companies that have been fully realised)."

**Owner of fix:** LP-side negotiation.

### Example C. GREEN finding

**Area:** 16. SCSp Law of 2013 compliance.

**Clause:** Sections 1.1 to 1.4.

**Quote:** "The Fund is a société en commandite spéciale established under Article 22-1 et seq. of the Luxembourg Law of 10 August 1915 on commercial companies, as amended."

**Standard:** Law of 10 August 1915.

**Severity:** GREEN.

**Issue:** The Fund's legal form, governing law, GP/LP structure, and registered office are correctly stated and consistent with Luxembourg SCSp practice. No action.

(No redline. No owner.)
