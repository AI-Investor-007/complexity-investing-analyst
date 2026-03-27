# Complexity Investing Analyst

A Claude skill for applying the **NZS Capital Resilience & Optionality
(R&O) framework** to analyse any listed company and produce a structured
investment memo.

Built for Indian listed equity analysis — smallcap and midcap — with
India-specific overlays. Usable on any global listed company.

---

## What This Skill Does

It takes multiple input sources, applies a structured qualitative
framework to classify a company on an S-curve, assesses management
quality and business durability, and produces a memo with a clear
classification, portfolio sizing recommendation, and monitoring trigger.

It then holds that analysis internally and asks for your own management
impressions and investor inputs — before showing you anything. It
compares the two independently formed assessments and surfaces where
they agree, where they diverge, and what each missed that the other
found.

The output is not a buy/sell recommendation. It is a classification
and decision support tool.

---

## The Framework

Built on **Complexity Investing** by Brinton Johns and Brad Slingerlend,
NZS Capital (2014, updated 2021).

Core argument: financial markets are complex adaptive systems best
explained by power laws, not normal distributions. Narrow predictions
of the future are dangerous. Capital should be allocated by balancing
**Resilience** (durable, long-duration compounders) with **Optionality**
(asymmetric, early-stage bets), while eliminating the unproductive
middle.

**Five classification zones:**

| Zone | What It Means | Position Size |
|---|---|---|
| Gambling | S-curve uncertain; binary outcome | <0.5% or avoid |
| Optional | S-curve forming; asymmetric upside | 0.5-2% tail |
| Resilient + Optional | Long-duration compounder | 3-5% core |
| Value Trap | S-curve concave; cheap but deteriorating | Avoid / exit |
| ROOTMO | Resilient core + optionality priced at zero | 3-5%+ |

**ROOTMO** (Resilience with Out-Of-The-Money Optionality) is the most
valuable classification — maximum analyst edge when the market is wrong
about both the Resilience and the Optionality simultaneously.

**NZS** (Non-Zero Sumness) — the best businesses create significantly
more value for their ecosystem (customers, suppliers, employees) than
they capture for themselves. High NZS predicts durability.

---

## What You Need Before Running This Skill

**Required:**
- A **NotebookLM notebook** for the company containing annual reports,
  earnings transcripts, investor presentations, DRHP, sell-side research
- A **Screener.in PDF** of the company page (print to PDF from screener.in)

**Improves the analysis significantly:**
- A **second NotebookLM notebook** for channel checks — competitor
  conversations, ex-employee inputs, customer feedback
- A **Value Picker forum URL** for the company (skill fetches it)
- Your own **management meeting notes**, sell-side conversations, or
  fellow investor inputs — written freely, no format required

If channel checks are unavailable, the skill automatically searches
AmbitionBox and Glassdoor.

---

## How It Works

The skill runs across four interactions:

**Interaction 1 — Invoke the skill**
Say: "Use the skill complexity-investing-analyst for [Company Name]"
The skill produces four NotebookLM prompts (pre-filled with the company
name) and a checklist of everything to gather. No analysis yet.

**Interaction 2 — Provide inputs**
Paste the NotebookLM outputs, upload the Screener PDF, provide the
Value Picker URL if available, and write any management or investor
impressions freely. The skill runs the full analysis internally —
without showing you the output yet.

**Interaction 3 — Targeted coverage check and output reveal**
The skill extracts signals from your impressions across ten assessment
dimensions. It asks only about dimensions not already covered —
nothing more. You provide gap-fills. The skill then reveals:
- Section 1: Full data-driven memo + four-part comparison output
- Section 2: Your impressions verbatim, with extracted signals

**Interaction 4 (optional) — Word export**
Type "export to Word" for a formatted .docx version.

---

## The Four-Part Comparison Output

The most distinctive feature of this skill:

- **Output A — Divergences:** Where data and your impression point in
  opposite directions. These are the things to think harder about before
  sizing a position.
- **Output B — Agreements:** Where both independently reach the same
  conclusion. Conviction builders.
- **Output C1 — Blind Spots:** What the data found that your prior
  missed. Things the evidence surfaced that you didn't account for.
- **Output C2 — Your Edge:** What your impression captured that no
  data source could — management body language, unexpected moments,
  a sell-side conversation that revealed something. Preserved explicitly
  as potentially high-value signal.

---

## India-Specific Design

Several adaptations for the Indian listed equity context:

- **Promoter nuance:** Centralised + long-term is acceptable for
  promoter-run companies. Centralised + short-term or self-interested
  is a red flag. The framework's default decentralisation preference
  applies primarily to hired-manager-run companies.
- **RPT threshold:** Any related-party transaction exceeding 5% of
  revenues is an automatic NZS deduction — the most direct evidence
  of value extraction from the ecosystem.
- **Liquidity as feature:** For smallcap stocks, illiquidity is itself
  a negative feedback loop that extends S-curve duration and depresses
  valuations. In the R&O framework this is a feature, not a bug — the
  liquidity discount is the price of admission for the duration premium.
- **Regulatory concentration:** Government as primary customer or
  price-regulated products are flagged as context variables, not
  automatic disqualifiers.

---

## Installation

**On claude.ai:**
1. Download the `.skill` file from this repository (Releases section)
2. Go to Claude.ai → Settings → Customize → Skills
3. Upload the `.skill` file
4. The skill is now active — invoke it by saying "Use the skill
   complexity-investing-analyst for [Company Name]"

**From source:**
Clone this repository. The skill folder contains:
- `SKILL.md` — main instructions and workflow
- `references/framework.md` — the R&O framework reference
- `references/prompts.md` — the four NotebookLM prompts

---

## File Structure

```
complexity-investing-analyst/
├── SKILL.md                      Main skill instructions
└── references/
    ├── framework.md              NZS Capital R&O framework reference
    └── prompts.md                Four NotebookLM extraction prompts
```

---

## Limitations

- Does not make buy/sell recommendations. Produces a classification
  and position size range. The investment decision is yours.
- Cannot access authenticated databases, broker platforms, or paid
  data sources. Relies on what you provide and public web sources.
- Cannot replace primary research. The User Input section requires
  you to have met management or have access to investors with direct
  knowledge. Without this, the comparison output is limited.
- Does not update itself. The framework reference file should be
  updated manually as you build a library of validated Indian examples.
- Classifications should be revisited at 6-12 months to assess accuracy.

---

## Feedback and Improvement

This skill is a work in progress. It has been tested on a small number
of Indian smallcap companies and is being refined through use.

If you are an investor who has used this skill, feedback on the
following is particularly valuable:

- Are the five NZS diagnostic questions sufficient for Indian companies,
  or are India-specific NZS signals missing?
- Is the S-curve classification matrix complete for Indian market archetypes?
- Are there better Indian-specific adversarial sources beyond Value Picker,
  AmbitionBox, and Glassdoor?
- Does the ten-dimension impression assessment cover the right ground,
  or are dimensions missing?
- Does the four-part comparison output serve its purpose as a decision
  support tool, or is something important absent?

Open an issue on this repository or reach out directly.

---

## Attribution

Framework: Brinton Johns and Brad Slingerlend, NZS Capital
Source: *Complexity Investing* (2014, updated January 2021)
Skill adaptation: Built for Indian listed equity analysis

This skill is an independent adaptation of the NZS Capital framework
for use with Claude. It is not affiliated with or endorsed by NZS Capital.
