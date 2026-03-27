# NotebookLM Prompts for Complexity Investing Analysis

These are the four prompts to run in NotebookLM before executing
the skill. When the user requests prompts for a company, reproduce
all four with [COMPANY NAME] replaced by the actual company name.

Financial data is NOT extracted via NotebookLM. The Screener.in
PDF uploaded directly into the chat is the authoritative source
for all financial trajectory and operational metrics.

---

## COMPANY SOURCES NOTEBOOK
Run Prompts 1 and 2 in the company sources notebook (ARs,
transcripts, presentations, DRHP, sell-side research).

---

### Prompt 1 — Management Language

```
Company: [COMPANY NAME]

Find verbatim quotes only — no paraphrases — where management
discusses the following. Cite the source document and year for
every quote. Where sources contradict each other, name both and
state what each says.

(1) How they decide to deploy capital — acquisitions, capex,
    buybacks, dividends, reinvestment.

(2) What will NOT change about customer needs over the next
    5–10 years.

(3) Pricing philosophy — do they describe pricing as a tool to
    grow the ecosystem or to maximise extraction from customers?

(4) Organisational structure — how do they describe decision-
    making authority? Is it centralised at the top or delegated
    to business unit leaders?

(5) Any instance where management describes sacrificing short-
    term margins or earnings for a long-term goal. Cite the
    specific decision, the cost accepted, and the stated rationale.

(6) How management describes relationships with suppliers and
    employees — as costs to be managed or as long-term partners?
```

---

### Prompt 2 — Ecosystem Data

```
Company: [COMPANY NAME]

Answer the following factual questions. Cite source and year for
every finding.

(1) Customer concentration: What percentage of revenue comes from
    the top 1, 3, and 10 customers? Has concentration increased
    or decreased over the last 3–5 years?

(2) Supplier relationships: Is there any evidence — from any
    source in this notebook — of how the company treats suppliers?
    Do suppliers have pricing power over the company, or does the
    company squeeze suppliers?

(3) Employee data: What does any source say about employee
    attrition, retention, satisfaction, or workforce stability?

(4) Adjacency investments: What new products, markets, or business
    lines has management invested in beyond the core business?
    For each, state the capital allocated and the year it began.

(5) Bear case: List every risk factor identified across all
    sources. Present each as a separate bullet. Do not blend or
    summarise them — list them individually and name the source
    for each.

(6) Gaps: Which of the following could you not answer reliably
    from the sources in this notebook — customer concentration
    from an independent source, pricing behaviour from a customer
    or competitor source, regulatory adverse orders, management
    capital allocation track record beyond stated intent, employee
    attrition data? For each gap, state why.
```

---

## CHANNEL CHECK NOTEBOOK
Run Prompts 3 and 4 in the channel check notebook (competitor
conversations, ex-employee interactions, customer feedback,
distributor checks).

---

### Prompt 3 — Channel Check Extraction

```
Company: [COMPANY NAME]

For each source in this notebook, extract observations separately
— do not blend sources. For each source, note the source type
(competitor / ex-employee / customer / distributor / other) and
then answer the following for that source specifically:

(1) What did this source observe about how decisions are made
    inside the company — who has authority, how fast decisions
    happen, whether strategy is driven from the top or from
    business units?

(2) What did this source say about the company's pricing
    behaviour — does the company price to create customer value
    or to extract maximum margin?

(3) What did this source say about the company's competitive
    strengths and weaknesses? Where does this source believe
    the company is winning or losing?

(4) What did this source say about the company's relationships
    with customers, suppliers, or partners — collaborative
    or extractive?

(5) Did this source mention anything about growth trajectory,
    product quality, or operational execution — positive
    or negative?

Present each source as a separate block. Use verbatim quotes
where available. Do not summarise across sources.
```

---

### Prompt 4 — Disagreements and Silences

```
Company: [COMPANY NAME]

Two questions:

(1) Do any channel check sources in this notebook contradict
    each other on any point? If yes, name both sources, state
    what each says, and identify the specific point of
    disagreement.

(2) What topics are completely absent from all channel check
    sources — things no source mentioned at all? List them.
    These silences may be as informative as the observations.
```

---

## SEQUENCING NOTE

Run Prompts 1 and 2 in the company sources notebook first.
Run Prompts 3 and 4 in the channel check notebook second.

Prompts 3 and 4 are self-contained — they do not require the
company source outputs to run.

Financial data (revenue, ROCE, margins, FCF, CAGR grids,
working capital, operational metrics, shareholding) comes from
the Screener.in PDF uploaded directly into the chat — not from
these prompts. Do not attempt to extract financial tables via
NotebookLM.

Paste all four outputs into the chat, clearly labelled by
prompt number, before invoking the skill.
