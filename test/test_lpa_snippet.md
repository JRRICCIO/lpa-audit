# Test LPA snippet · Acme Capital Partners SCSp

**Use:** Synthetic LPA passages crafted with known issues for testing the Ikhor LPA Audit skill. Expected findings annotated at the bottom.

---

## Section 1.1 Definitions (excerpts)

"**Preferred Return**" means an amount equivalent to a return of 8% per annum, simple interest, calculated on contributed Capital Commitments from the date of the Capital Call to the date of the relevant distribution.

"**Hurdle**" means the Preferred Return.

"**Key Person**" means each of [Founder A] and [Founder B].

## Section 6.1 Management Fee

The General Partner shall be entitled to a Management Fee of 2.0% per annum of Aggregate Commitments during the Investment Period and 2.0% per annum of Aggregate Commitments thereafter until the Fund is wound up.

## Section 7.2 GP Commitment

The General Partner shall make a Capital Commitment to the Fund in such amount as the General Partner determines, in its sole discretion, to be appropriate. The GP Commitment may be funded by way of fee waiver or borrowed funds.

## Section 9.3 Key Person Event

If two or more of the Key Persons cease to be employed by the General Partner due to death or termination of employment, the General Partner shall promptly notify the Limited Partners. The Limited Partner Advisory Committee may, at its discretion, suspend the Investment Period.

## Section 13.2 Liquidity

The Fund is an open-ended structure. Limited Partners may request redemption on a quarterly basis with 90 days' prior written notice. In the event of stressed market conditions, the General Partner may, in its sole discretion, suspend redemptions.

## Section 13.4 Indemnification

The General Partner, its affiliates, officers, directors, employees and agents shall be indemnified and held harmless by the Fund from and against any and all claims, damages and liabilities arising out of or in connection with the performance of their duties for the Fund, except in cases of fraud as finally adjudicated by a court of competent jurisdiction.

## Section 14.5 LPAC

The Fund shall have a Limited Partner Advisory Committee composed of representatives of three Limited Partners selected by the General Partner. The LPAC may provide advice to the General Partner on matters submitted to it, but shall have no consent or approval rights with respect to any action of the General Partner.

## Section 15.3 Conflicts of Interest

In the event of a conflict of interest, the General Partner may resolve the matter in its sole discretion, having regard to the interests of all parties.

## Section 16.1 Side Letters

The General Partner is authorised to enter into side letters with Limited Partners on such terms as the General Partner determines. The terms of side letters shall be confidential between the General Partner and the relevant Limited Partner.

## Section 19.2 Removal of the GP

The General Partner may be removed only by a vote of 95% of the Limited Partners and only following a final, non-appealable court judgment of fraud or gross negligence.

## Section 20.4 Loan Origination

The Fund may originate loans to portfolio companies and third parties as the General Partner determines. The Fund's portfolio shall be subject to such concentration limits as the General Partner shall establish from time to time.

---

## Expected findings (the answer key)

1. **Hurdle / Preferred Return: AMBER.** Simple interest, not compounding. Below ILPA standard. Should be compounded.
2. **Management Fee: AMBER.** No step-down at end of Investment Period. ILPA recommends step-down to invested-capital basis.
3. **GP Commitment: RED.** "In such amount as the GP determines" with fee-waiver or borrowed funding. No skin in the game.
4. **Key Person Event: AMBER-to-RED.** Trigger lacks dedication-of-time prong. Suspension is LPAC-discretionary, not automatic. No cure period stated. No remediation termination.
5. **Liquidity Management Tools: RED.** Open-ended fund with only suspension. AIFMD II requires at least two LMTs from the harmonised EU list.
6. **Indemnification: RED.** Carveout is fraud only. Excludes gross negligence, willful misconduct, material breach, securities law violations. Not enforceable in Luxembourg for gross negligence and below ILPA market.
7. **LPAC: RED.** Advisory only, no consent rights. Below ILPA standard.
8. **Conflicts of Interest: RED.** GP resolves in sole discretion. No LPAC consent. Below ILPA standard.
9. **Side Letters: RED.** No MFN provision, no disclosure to other LPs. Below ILPA standard.
10. **Removal of GP: RED.** 95% threshold + court judgment requirement = effectively impossible. Below market and unworkable.
11. **Loan Origination: RED.** No 5% retention, no concentration limit specified, no credit risk policy reference. Non-compliant with AIFMD II.
12. **Document silent on: AIFM identity, leverage cap and method, delegation, reporting cadence, default mechanics, transfer regime, recycling, valuation methodology, fiduciary duty clarification, LP communication rights, change of GP control consent, LPAC in-camera rights, LP list, clawback (if applicable).** Each silence on a mandatory item = RED.

**Overall verdict expected:** Do not sign. Material edits required across multiple ILPA and AIFMD II areas.

**Top 3 most material findings:**
1. RED - Liquidity Management Tools missing (regulatory non-compliance for open-ended structure)
2. RED - Indemnification too broad (below ILPA market, unenforceable on gross negligence under Lux law)
3. RED - LPAC has no consent rights (governance failure below ILPA Principles 3.0)
