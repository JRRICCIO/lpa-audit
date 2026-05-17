# Regulatory sources to monitor

A practitioner-grade list of authoritative sources for AIFMD II, Luxembourg fund formation, and ILPA market standards. The skill reads this file when performing the regulatory currency check, to know where to look for updates since the skill's compilation date.

Each source is tagged with the type of updates that matter and the typical cadence of publication.

## EU-level regulators and authorities

### ESMA (European Securities and Markets Authority)
- Homepage: https://www.esma.europa.eu/
- Q&As on AIFMD: https://www.esma.europa.eu/document/qa-application-aifmd
- Press releases and consultations: https://www.esma.europa.eu/press-news
- **Updates to look for:** RTS finalisation (loan-originating AIFs, LMTs, leverage calculation), Q&A updates, ESMA Guidelines on delegation and substance, ELTIF 2.0 technical standards.
- **Cadence:** RTS in waves; Q&As updated quarterly.

### EBA (European Banking Authority)
- Homepage: https://www.eba.europa.eu/
- **Updates to look for:** Single rulebook updates affecting bank-affiliated AIFMs, MREL, prudential requirements for AIFM groups, ESG risk supervision.
- **Cadence:** Periodic.

### European Commission (DG FISMA)
- Capital Markets Union page: https://finance.ec.europa.eu/capital-markets-union-and-financial-markets_en
- **Updates to look for:** Level 2 delegated acts under AIFMD II, ELTIF 2.0 Level 2, SFDR review outcomes.
- **Cadence:** Less frequent but high impact.

## Luxembourg authorities

### CSSF (Commission de Surveillance du Secteur Financier)
- Homepage: https://www.cssf.lu/
- Circulars page: https://www.cssf.lu/en/regulatory-framework/
- FAQs: https://www.cssf.lu/en/documents-and-publications/
- **Updates to look for:** New circulars on AIFMD II implementation, FAQs on Annex IV reporting, substance circular updates (the substance test referenced in Circular 18/698 and successors), pre-marketing rules, depositary requirements.
- **Cadence:** Multiple per year; circulars are dated YY/NNN.

### Legilux (Luxembourg official journal)
- Homepage: https://legilux.public.lu/
- **Updates to look for:** Bills of law (Memorial A), regulations amending the 1915 Law (SCSp), the 2013 AIFM Law, and tax law affecting funds.
- **Cadence:** Continuous.

### Luxembourg for Finance
- Homepage: https://www.luxembourgforfinance.com/
- **Updates to look for:** Practitioner-grade summaries of new regulation, sector statistics, market notes.
- **Cadence:** Weekly to monthly.

## Market standards bodies

### ILPA (Institutional Limited Partners Association)
- Homepage: https://ilpa.org/
- Industry guidance: https://ilpa.org/industry-guidance/
- News: https://ilpa.org/news/
- **Updates to look for:** Principles updates (currently 3.0), Model LPA refreshes, guidance on NAV facilities, GP-led secondaries, continuation funds, capital call notice template, fee reporting template, subscription line guidance.
- **Cadence:** Quarterly major publications; rolling notes.

### INREV (European Association for Investors in Non-Listed Real Estate Vehicles)
- Relevant if the LPA is for a real estate fund.
- Homepage: https://www.inrev.org/

### Invest Europe
- Homepage: https://www.investeurope.eu/
- **Updates to look for:** Industry-position papers on EU regulation, retail-eligible private markets, ELTIF 2.0 adoption.

## Practitioner publications (secondary sources, verified by primary above)

These are useful for quick reads and trend signals but should be cross-checked against the primary sources above before relying on them.

- Loyens & Loeff insights: https://www.loyensloeff.com/insights/
- Arendt & Medernach insights: https://www.arendt.com/jcms/p_arendt_news_pubs/
- Elvinger Hoss publications: https://elvingerhoss.lu/publications
- Linklaters AIFMD: https://www.linklaters.com/en/insights/publications/aifmd
- Clifford Chance briefings on AIFMD II
- Arthur Cox AIFMD II series
- CMS Luxembourg newsflashes
- Dechert "AIFMD 2.0" series
- Maples Group Luxembourg fund formation alerts
- Funds Europe, Private Equity International, Private Debt Investor

## How to use this file at runtime

When the skill performs the regulatory currency check:

1. Read the compilation date from `CHANGELOG.md`.
2. If the model has web search or web fetch tools, search the EU-level and Luxembourg sources first for material updates since the compilation date. Focus on:
   - ESMA Q&A on AIFMD updates
   - CSSF new circulars after Circular 25/901
   - ESMA final RTS publications (the ones flagged as "pending" in the changelog)
   - ILPA Principles or Model LPA refreshes
3. If a material update is found, incorporate the new parameter into the relevant review area for the audit, and note the update in the scope statement.
4. If web tools are not available, declare this in the scope statement: "Regulatory currency check could not be performed in this session. The audit reflects rules as of [compilation date]. Recommend re-checking ESMA, CSSF, and ILPA for updates before close."
5. Always cite the URL of any update incorporated. Tag with `[verify]` if the model is uncertain whether the source is the primary authority.

## What counts as a "material update"

Material updates include any of the following:

- Final RTS where only draft RTS existed at compilation (changes the binding rule from "as currently drafted" to "as adopted").
- New ESMA Q&A clarifying a previously ambiguous AIFMD II rule.
- New CSSF circular adding or modifying obligations on AIFMs, depositaries, or AIFs.
- New ILPA Principles version or Model LPA refresh.
- EU-level political decision changing the effective date of any AIFMD II provision.
- Court decision (CJEU, Luxembourg administrative courts) affecting substance, delegation, or fund structuring.

Cosmetic clarifications, press releases without normative content, and non-material consultations are NOT material updates for this purpose.
