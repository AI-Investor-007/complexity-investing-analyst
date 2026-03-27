---
name: complexity-investing-analyst
description: >
  Apply the NZS Capital Resilience & Optionality (R&O) complexity investing
  framework to analyse any company — listed or unlisted, Indian or global.
  Trigger whenever the user asks to evaluate a stock or business through the
  lens of S-curves, NZS, ROOTMO, Resilience/Optionality classification, or
  complexity investing. Also trigger for phrases like "where does X sit on
  the S-curve", "is this a value trap or resilient compounder", "apply the
  R&O framework", "classify this company using complexity investing", "NZS
  analysis of Y", "does this management think long-term", "is this business
  creating or extracting value from its ecosystem", or any request to assess
  management quality, business model durability, or optionality through a
  qualitative framework. Always use this skill even for quick classification
  requests — the framework cannot be reliably replicated ad hoc.
---

# Complexity Investing Analyst

A skill for applying the NZS Capital Resilience & Optionality (R&O)
framework to analyse any company and produce a structured investment memo.

Inspired by: Brinton Johns and Brad Slingerlend, NZS Capital
Source:      Complexity Investing (2014, updated 2021)
Framework:   Resilience & Optionality — a complexity-based capital
             allocation model emphasising adaptability, NZS, S-curve
             duration, and the balance between Resilience and Optionality
             in both companies and portfolios.

---

## QUICK START — READ THIS FIRST IF YOU ARE NEW TO THIS SKILL

This skill applies the NZS Capital Resilience & Optionality framework
to analyse any company and produce a structured investment memo.
It runs across four interactions — not one.

**What is NZS?**
NZS stands for Non-Zero Sumness. The best businesses create
significantly more value for their ecosystem — customers, suppliers,
employees, partners — than they capture for their own treasury. As
information transparency increases, companies that extract value from
their ecosystem become increasingly vulnerable to disruption. NZS
is both a business quality signal and a durability predictor.

**What is ROOTMO?**
ROOTMO stands for Resilience with Out-Of-The-Money Optionality.
It is the most valuable classification in this framework — the point
of maximum analyst edge. A ROOTMO company has a durable, cash-
generative Resilient core AND an adjacency bet the market is pricing
at or near zero. The analyst edge is maximum when both mispricings
are present simultaneously. ROOTMO is distinct from a Value Trap:
the new S-curve must be built from strength, not desperation.
Full definition is in references/framework.md.

---

**THE FIVE STEPS:**

**STEP 1 — INVOKE THE SKILL**
Say: "Use the skill complexity-investing-analyst for [Company Name]"
The skill produces four NotebookLM prompts and a full input checklist.
Nothing is analysed yet.
*Why: The prompts are designed to extract specific signals the framework
needs — verbatim management language, ecosystem data, and adversarial
channel check observations — in a way that preserves their independence
before the skill synthesises them.*

**STEP 2 — GATHER YOUR INPUTS**
Collect and return with the following:

REQUIRED:
A. NotebookLM output — Prompts 1 and 2 from your company sources
   notebook (ARs, transcripts, presentations, DRHP, sell-side research)
B. Screener.in PDF — print the company page to PDF and upload directly.
   This is the sole source of all financial data in the analysis.

PROVIDE IF AVAILABLE:
C. NotebookLM output — Prompts 3 and 4 from your channel check notebook
   (competitor conversations, ex-employee inputs, customer feedback).
   If absent: the skill auto-searches AmbitionBox and Glassdoor.
D. Value Picker forum URL — paste the link. Skill fetches it directly.
E. Your bear case — the specific reasons you think you might be wrong.
   Not your view. Your doubts.
F. Any regulatory orders, adverse filings, or legal proceedings.
G. User Input — write freely about any of the following:
   - Your own management meeting or concall interaction
   - Conversations with sell-side analysts (note if bullish/bearish)
   - Conversations with fellow investors (note if they are holders)
   No format required. Any length. The skill extracts signals from it.

Paste everything into the chat, labelled A through G.
Upload the Screener PDF directly. Then say: "Run the analysis."

*Why two notebooks for NotebookLM: Company sources are systematically
tilted toward the bull case — they are produced by or for the company.
Channel checks are adversarial. Keeping them in separate notebooks
ensures the adversarial signal arrives at the skill unblended, so
contradictions surface rather than disappear into synthesis.*

**STEP 3 — USER INPUT EXTRACTION**
The skill runs the full analysis internally — you do not see the output
yet. It then reads your User Input (item G), extracts signals across
ten assessment dimensions, and presents a targeted coverage check
asking only about dimensions not covered in your input.
If you have no User Input, type "no impression" and the skill proceeds.
*Why the output is held: if you saw the skill's verdict before answering,
your responses would unconsciously anchor to it. The two assessments
must be formed independently to preserve the value of the comparison.*

**STEP 4 — RECEIVE THE OUTPUT**
The skill compares your User Input signals against its internal analysis:
- Section 1: Full data-driven memo + four-part comparison output
- Section 2: Your User Input verbatim, for audit trail

**STEP 5 — OPTIONAL WORD EXPORT**
Type "export to Word" for a formatted .docx version.
Note: this requires additional processing time and tokens.

That is the complete workflow. The skill handles everything else.

---

## INTERACTION DESIGN

This skill runs across four distinct interactions. Do not collapse them.

Interaction 1: Skill invoked → prompts generated → inputs requested
Interaction 2: User returns with inputs → full analysis runs internally
               → User Input extracted → coverage check presented
Interaction 3: User returns with coverage check answers
               → comparison runs → full output revealed
Interaction 4: Optional → user triggers Word export

---

## Step 0A — Default Opening Move (Always Run First)

When the skill is invoked with a company name, this is always the
first action — before any analysis, before reading framework.md.

### Part 1: Produce the NotebookLM Prompts

Read references/prompts.md and reproduce all four prompts in full
with [COMPANY NAME] replaced by the actual company name throughout.

Present in two clearly separated blocks:

COMPANY SOURCES NOTEBOOK
Prompt 1 — Management Language     [full prompt with company name]
Prompt 2 — Ecosystem Data          [full prompt with company name]

CHANNEL CHECK NOTEBOOK
Prompt 3 — Channel Check Extraction    [full prompt with company name]
Prompt 4 — Disagreements and Silences  [full prompt with company name]

### Part 2: Nudge for All Direct Inputs

Immediately after the prompts, present the following nudge exactly:

---
"Run the prompts above in their respective NotebookLM notebooks
and paste the outputs back here when ready, clearly labelled.

Alongside the NotebookLM outputs, please also provide:

REQUIRED:
- Screener.in PDF for [COMPANY NAME] — upload directly into the chat.
  This is the authoritative source for all financial data.

PROVIDE IF AVAILABLE:
- Value Picker forum URL — paste the link, the skill fetches it.
- Channel check notebook output (Prompts 3 and 4) if you have one.
  If not, the skill will automatically search AmbitionBox and Glassdoor.

USER INPUT (provide anything you have — no format required):
- Your own management meeting, concall, or AGM notes
- Conversations with sell-side analysts — note if bullish or bearish
- Conversations with fellow investors — note if they are holders
Write freely. Any length. The skill extracts what it needs.

OPTIONAL BUT VALUABLE:
- Your bear case — the specific reasons you think you might be wrong
  about this company. Not your view. Your doubts.
- Any regulatory orders, adverse filings, or legal proceedings you
  are aware of that may not appear in standard sources.

Note: Type 'export to Word' after the analysis to generate a
formatted Word document. This requires additional processing."
---

### Part 3: Wait

Do not begin analysis. Do not read framework.md yet.
Wait for the user to return with all inputs.

---

## Step 0 — Pre-Read (Mandatory, Before Analysis Begins)

Once inputs are received, read references/framework.md in full
before beginning any analysis. Do not proceed without it.

---

## Step 1 — Input Handling

Identify which inputs are present before proceeding.

### Input Type A: Company Sources Output
NotebookLM output from Prompts 1 and 2 — synthesised from ARs,
transcripts, investor presentations, DRHP, sell-side research.
Role: What management says. Systematically tilted toward bull case.
Treat accordingly.

### Input Type B: Channel Check Output
NotebookLM output from Prompts 3 and 4 — competitor conversations,
ex-employee interactions, customer feedback, distributor checks.
Role: Adversarial signal. Where A and B conflict, the conflict is
information — adjudicate, do not resolve silently.

### Input Type B2: Secondary Adversarial Sources
Value Picker forum content (fetched from URL), AmbitionBox reviews
(web searched), Glassdoor reviews (web searched).
Role: Secondary adversarial — same weight category as B but labelled
as secondary (anonymous/unverified) vs. primary channel checks
(direct conversations). Flag this distinction in source attribution.
If no channel checks and no Value Picker URL: automatically web
search AmbitionBox and Glassdoor as part of Step 1.5 G6 gap check.
Do not wait to be asked.

### Input Type C: Screener.in PDF
The Screener.in PDF uploaded directly into the chat.
Role: AUTHORITATIVE source for all financial trajectory and
operational metrics. Supersedes any financial data from NotebookLM.
Read the following from the Screener PDF:
- Revenue trajectory and growth rates (annual series)
- ROCE, OPM, PAT margin (annual series)
- Free cash flow and reinvestment ratios
- CAGR grids (3yr, 5yr, 10yr for sales, profit, ROE)
- Working capital metrics (debtor days, inventory days, CCC)
- Operational metrics from Insights section (market share,
  installed capacity, dealer count, customer touchpoints)
- Shareholding pattern

### Input Type D: Direct Uploads or Pastes
Any other document — AR, concall note, news article, regulatory order.
Role: Supplementary. Weight by source type — company-controlled =
Input A weight; independent/adversarial = Input B weight.

### Input Type E: User Input
Free-form text from the user covering any combination of:
- Management interaction (meeting, concall, AGM, site visit)
- Sell-side analyst conversation
- Fellow investor conversation

Role: Human impression input — the only source type that captures
signals no document can surface. Processed in Step 3.

Source priority within User Input:
- Management interaction: highest priority — direct and primary
- Sell-side analyst: secondary — structurally optimistic; note
  any stated bias (bull/bear/holder of covered stock)
- Fellow investor: secondary — note if holder; note any other
  known bias. Otherwise treat as peer input.

No arithmetic weighting. The skill reads the debrief, notes the
source type per observation, flags stated biases, and applies
qualitative priority — management interaction anchors the impression
assessment; everything else is contextual and supplementary.

### Input Inventory

State before beginning analysis:

Input A  (Company Sources):    Present / Absent
Input B  (Channel Checks):     Present / Absent / Partial (n checks)
Input B2 (Secondary Adv.):     Value Picker / AmbitionBox / Glassdoor / None
Input C  (Screener PDF):       Present / Absent
Input D  (Direct uploads):     Present / Absent / [describe]
Input E  (User Input):         Present / Absent
                               [Management meeting? Sell-side? Investor?
                                Any holder bias noted?]

If Input B and B2 are both absent, flag prominently.
If Input C is absent, flag prominently — financial trajectory will
rely on NotebookLM extraction which is less reliable.
If Input E is absent, impression assessment will be skipped and
the comparison output will be limited to C1 (blind spots only).

---

## Step 1.5 — Gap Identification and Targeted Web Search

Mandatory. Run before Step 2 regardless of input richness.

### Six Gap Questions

G1. Enough management language to score allocator vs. operator
    reliably? Or only IR-polished quotes without depth?
    Status: COVERED / THIN / ABSENT

G2. 5-7 year revenue and ROCE trajectory available?
    [If Screener PDF present: COVERED automatically]
    Status: COVERED / THIN / ABSENT

G3. Pricing behaviour evidenced from customer or competitor
    sources — not just management's description of it?
    Status: COVERED / THIN / ABSENT

G4. Customer and supplier concentration data from independent
    sources, not only company-controlled disclosures?
    Status: COVERED / THIN / ABSENT

G5. Regulatory filings, adverse orders, legal proceedings, or
    competitive actions not covered in either notebook?
    Status: COVERED / THIN / ABSENT

G6. Channel checks covering all three adversarial source types
    (competitor, ex-employee, customer)?
    If absent or partial: automatically web search AmbitionBox
    and Glassdoor. Do not wait to be asked.
    Status: COVERED / THIN / ABSENT

### Targeted Web Search

For every gap marked THIN or ABSENT, run targeted web search.
Construct query from the specific gap, not a generic prompt.

Gap | Example Search Query
G1  | "[CEO name] capital allocation" OR "[company] shareholder letter"
G2  | "[company] revenue ROCE history" [only if Screener PDF absent]
G3  | "[company] customer complaints pricing" OR "[competitor] vs [company]"
G4  | "[company] customer concentration top customer revenue"
G5  | "[company] SEBI order penalty litigation"
G6  | "[company] AmbitionBox reviews" OR "[company] Glassdoor reviews"

Classify each web search result:
- Company-controlled → Input A weight
- Independent / adversarial → Input B weight, labelled secondary
- Unverifiable / opinion → flag and discount

Record unresolved gaps — these become explicit flags in memo output.

---

## Step 2 — Analysis Protocol (Internal — Do Not Show Output Yet)

Run all six steps internally. Hold the output. Do not show the user
anything until the User Input extraction and coverage check are complete.

For every finding, attribute to source:
[A] company sources | [B] channel checks | [B2] secondary adversarial
[C] Screener PDF | [W] web search | [U] unresolved

### 2.1 S-Curve Positioning

- Slope: Early convex / Clearly convex / Flattening /
         Turning concave / Clearly concave
- Stage: Early / Growth / Mid-cycle / Mature
- Zone:  Gambling | Optional | Resilient + Optional |
         Value Trap | ROOTMO

Assess slope from Screener PDF financial trajectory [C] as primary
source. Cross-check against channel check signals on growth
durability [B/B2]. Note divergence between financial data and
channel check sustainability signals explicitly.

Key diagnostic: Flat and steady growth rate over long period
[Resilient signal] vs. high-growth spike followed by deceleration
[fragile signal]. Source every assertion.

### 2.2 Quality Assessment

Score each dimension High / Medium / Low. Every score must cite
a source. One-sentence justification per score.

Dimension           | Score (H/M/L) | Source | Evidence
CEO: allocator vs. operator       |               |        |
Decentralised decision making     |               |        |
Long-term thinking                |               |        |
Culture of innovation/adaptability|               |        |

Adjudication: If [A] and [B/B2] conflict, record both, explain
weighting, do not split the difference silently.

India-specific: Apply promoter nuance from framework.md Section 4.
RPTs exceeding 5% of revenues = automatic NZS deduction.

Overall Quality verdict: High / Medium / Low

### 2.3 Growth / NZS Assessment

Answer all five NZS diagnostic questions from framework.md Section 3.
Cite source per answer. Flag [A] vs [B/B2] divergence on each.

1. Stakeholder value creation     [A: ] [B/B2: ] [Divergence: ]
2. Win-win business models        [A: ] [B/B2: ] [Divergence: ]
3. Long-term orientation          [A: ] [B/B2: ] [Divergence: ]
4. Resilience indicators          [A: ] [B/B2: ] [Divergence: ]
5. Optionality bets               [A: ] [B/B2: ] [Divergence: ]

TAM: Large / Constrained / Unclear [source]
Feedback loop: Negative / Positive / Mixed [source]
S-curve stacking: Evidence / Aspiration / None [source]

NZS verdict: Strong / Moderate / Weak

### 2.4 Context Assessment

This section uses only framework-native valuation language.
Do not import traditional sell-side multiples (P/E, EV/EBITDA,
EV/Sales, target prices, peer comparisons). Those answer a
different question — is this cheap relative to peers? — which
is not the R&O framework's question. The framework's question
is: what is the market pricing, and is that fragile?

**Valuation fragility test (mandatory)**
How many narrow predictions does this valuation require, and
what type?
- Duration predictions: most reliable; NZS and negative feedback
  loops make these estimable with reasonable confidence
- Profitability recovery predictions: medium reliability; depends
  on cycle vs. structure diagnosis
- New market / vertical success predictions: most fragile; require
  the narrowest precision; should never anchor a large position

State prediction count and type. Conclude:
"This valuation is [low/medium/high] fragility because it requires
[n] predictions of [type]."

**Implied return (mandatory)**
FCF yield [from Screener PDF] + expected long-term FCF/share
growth rate = implied expected return.
State components and total. Flag if FCF conversion has deteriorated
significantly vs. prior years.

**Market pricing signal (mandatory)**
Is Optionality being priced at near-zero by the market?
Answer: Yes / No / Partially.
If Yes or Partially: name the specific Optionality the market is
discounting. This is the bridge into the ROOTMO assessment.

**Ecosystem tailwinds / headwinds**
Structural only — not cyclical. What will not change over the
next decade, and what is structurally shifting?

**India-specific overlays**
- Promoter capital allocation track record [A, W] — actual decisions
- RPT check — flag if RPTs exceed 5% of revenues [source]
- Liquidity band — smallcap illiquidity as negative feedback loop
  feature; liquidity discount is the price of duration premium
- Regulatory concentration risk [G5 result]

### 2.5 Classification and Sizing

Primary classification:
Gambling | Optional | Resilient + Optional | Value Trap | ROOTMO

Classification | Position Size | Logic
Resilient + Optional | 3-5% concentrated | Core; few predictions required
ROOTMO               | 3-5%+ room to run | Maximum conviction; double mispricing
Pure Optionality     | 0.5-2% tail       | Asymmetric; survivable if wrong
Gambling             | <0.5% or avoid    | Binary; narrow prediction required
Value Trap           | Avoid / exit      | Widening outcomes; commitment risk

Classification risk: The single factor whose change would reclassify
this company to an adjacent zone. This is the monitoring trigger.

Common mistake check (framework.md Section 6):
- Value trap masquerading as value?
- Optionality name being sized for head position?
- Stuck-in-the-middle with no S-curve stacking ability?

### 2.6 One-Line Verdict (Internal)

"[Company] is [classification] — [core reason], but [tension].
Monitor [specific trigger]."

Hold this verdict internally. Do not reveal yet.

---

## Step 3 — User Input Assessment

### Part 3A: Extract from User Input

If Input E is present, read it in full. Map every passage to one
or more of the ten assessment dimensions. For each dimension assign:

- Directly Observed (DO): topic came up explicitly; clear impression
  available; cite the specific passage
- Implied: topic not raised directly but a reasonable inference is
  possible from adjacent signals; cite passage and state inference
- Absent: no coverage and no inference possible

Note source type per passage: Management / Sell-side / Investor.
Flag stated biases: "holder [n]% position", "covered analyst",
"known bull on this sector" etc. Do not discount arithmetically
— flag for the reader's awareness.

The ten dimensions and what to look for:

D1  Capital allocation instinct
    Language about deploying cash, acquisitions, capex, buybacks,
    reinvestment priorities

D2  Intellectual honesty under pressure
    How management or the source handled hard questions; deflections;
    moments of candour or evasiveness; body language signals [YM only]

D3  Long-term anchor
    Articulation of what will NOT change about customers; decade-
    horizon thinking; resistance to short-termism

D4  Ecosystem orientation
    How management / source describes customers, suppliers, dealers,
    partners — as constituents or as channels/costs

D5  Pricing philosophy
    Any mention of pricing decisions, margin sacrifice, price war
    resistance. Note: pricing power language is a warning sign.

D6  Negative feedback loop awareness
    Awareness of what moderates their own growth; humility about
    ceiling; self-correcting instincts vs. unchecked confidence

D7  New S-curve articulation
    Description of specific adjacency bets with conviction — not
    investor-day language but genuine operational commitment

D8  Experimentation comfort
    References to small bets, failures as learning, tolerance for
    uncertainty in new initiatives

D9  Resilience as foundation for Optionality
    Does the new bet language come from strength (funded by resilient
    core) or from pressure (diversifying away from stressed core)?
    This is the ROOTMO vs. Value Trap discriminator.

D10 Overall conviction
    Gut read on whether management has imagination AND discipline
    to build the next S-curve — not just vision but patient execution

After mapping, produce a coverage summary:

COVERED (Directly Observed): [list dimensions]
COVERED (Implied):           [list dimensions with inference noted]
ABSENT:                      [list dimensions]

If Input E is absent, all ten dimensions are Absent.
Proceed to Part 3B with all ten as gaps.

### Part 3B: Targeted Coverage Check

Present only Absent dimensions to the user. Do not re-ask
dimensions already Directly Observed or Implied.

Open with:

"The analysis is complete internally. Based on your User Input,
I have signals on the following dimensions:
COVERED: [list]

These dimensions were not covered. If you have any impression —
even a vague one — share it in one or two sentences. Note the
source type (management / sell-side / investor) and any known bias.
If you have no read at all, say 'no read':

[For each Absent dimension: name, one-line description of what
to look for, prompt for source and bias]

If you have no User Input at all, type 'no impression' and I
will proceed to the output."

Wait for responses before proceeding to Step 4.

### Part 3C: Absent Dimension Handling

For every dimension marked Absent after Parts 3A and 3B:
- Score: Not Sure
- Excluded from impression assessment entirely
- Flagged in output: "No user input on [dimension] — excluded"

Do not infer scores for Absent dimensions from data signals.
The impression assessment must remain independent of the
data-driven verdict.

---

## Step 4 — Comparison and Output Reveal

### 4.1 Compute Impression Assessment

For each dimension with coverage, derive a qualitative rating:
High / Medium-High / Medium / Medium-Low / Low / Not Sure

Evidence type modulates confidence, not the rating itself:
- Directly Observed: full confidence in the rating
- Implied: rating is provisional — flag as inferred
- Absent: excluded

Source priority within User Input:
- Management interaction anchors the assessment for that dimension
- Sell-side and investor inputs are contextual and supplementary
- Holder bias is flagged visibly but does not change the rating
  arithmetically — the reader adjudicates

Derive implied classification from the qualitative pattern:
Gambling / Optional / Resilient / Value Trap / ROOTMO

If more than three dimensions in a group are Absent, that group's
implied classification is flagged as unreliable.

Special flag: If a holder's view on a specific dimension diverges
significantly from a non-holder's view, flag this explicitly as
bias potentially colouring that dimension. Do not average silently.

### 4.2 Run Four-Part Comparison

Compare impression-implied classification against the internally
held data-driven verdict:

Output A — Divergences
Where data verdict and impression verdict point in opposite
directions. Present as:
"Data suggests [X]. Your assessment suggests [Y].
Think harder about this — specifically [what to investigate]."
These are priority action items, not conclusions.

Output B — Agreements
Where both inputs independently reach the same conclusion.
Present briefly — conviction builders but not the focus.

Output C1 — Blind Spots (Visible to skill only)
Findings from data, channel checks, or web search that have
no counterpart in the User Input — things the evidence found
that the user's prior did not account for.
"The data surfaced [X] which your input did not address.
Consider whether this changes your view."

Output C2 — Your Edge (Visible to user only)
Qualitative signals from the User Input that no data source
could surface — management body language, unexpected moments,
a comment that revealed something about character.
"You flagged [X]. This cannot be verified from data sources
but is preserved as potentially high-value signal."

Special flag: If a source identified as a holder diverges
significantly from other sources on a specific dimension,
flag explicitly — do not blend.

### 4.3 Reveal Full Output

Now reveal the complete output in two sections.

---

## Step 5 — Full Output Format

Use standard markdown only — bold headers and --- dividers.
No Unicode box-drawing characters. Bold headers and --- dividers
survive copy-paste into email, Google Docs, and Word cleanly.

After the full output add:
"Type 'export to Word' for a formatted .docx — note this
requires additional processing."

---

**SECTION 1: DATA-DRIVEN ANALYSIS**

---

**COMPLEXITY INVESTING MEMO**

Company: [Name] | [Exchange: Ticker]
Date: [Date]
Classification: [Zone]
Confidence: High / Medium / Low

*This memo applies the NZS Capital Resilience & Optionality framework,
inspired by Brinton Johns & Brad Slingerlend, Complexity Investing
(2014, updated 2021). The framework views financial markets as complex
adaptive systems best explained by power laws, not normal distributions.
Capital is allocated by balancing Resilience (durable long-duration
compounders) with Optionality (asymmetric early-stage bets), eliminating
the unproductive middle. NZS (Non-Zero Sumness) is the principle that
the best businesses create significantly more value for their ecosystem
— customers, suppliers, employees — than they capture for themselves.
ROOTMO (Resilience with Out-Of-The-Money Optionality) is the most
valuable classification: a Resilient core with adjacency bets priced
at near-zero by the market.*

---

**INPUT INVENTORY**

Company Sources [A]: Present / Absent
Channel Checks [B]: Present / Absent / Partial (n checks)
Secondary Adv. [B2]: Value Picker / AmbitionBox / Glassdoor / None
Screener PDF [C]: Present / Absent
Direct uploads [D]: Present / Absent / [describe]
User Input [E]: Present / Absent [Management / Sell-side / Investor]
Web search gaps filled: [list]
Unresolved gaps: [list]

---

**1. S-CURVE POSITION**

Zone: [label] | Slope: [label] | Stage: [label]

[3-4 sentences with source attribution]

A says: [finding]
B/B2 says: [finding]
Divergence: Yes / No / Silent

---

**2. QUALITY ASSESSMENT**

Allocator vs. Operator: [H/M/L] [source] — [one line]
Decentralised Decision Making: [H/M/L] [source] — [one line]
Long-Term Thinking: [H/M/L] [source] — [one line]
Innovation / Adaptability: [H/M/L] [source] — [one line]
Key A vs B conflict: [describe if present]
Overall Quality: High / Medium / Low

---

**3. NZS / GROWTH ASSESSMENT**

(1) Stakeholder value creation: [A: ] [B/B2: ] [Divergence: ]
(2) Win-win business model: [A: ] [B/B2: ] [Divergence: ]
(3) Long-term orientation: [A: ] [B/B2: ] [Divergence: ]
(4) Resilience indicators: [A: ] [B/B2: ] [Divergence: ]
(5) Optionality bets: [A: ] [B/B2: ] [Divergence: ]

TAM: [Large / Constrained / Unclear] [source]
Feedback Loop: [Negative / Positive / Mixed] [source]
S-Curve Stacking: [Evidence / Aspiration / None] [source]
NZS Verdict: Strong / Moderate / Weak

---

**4. CONTEXT**

Valuation fragility: [n predictions | types | Low/Medium/High]
Implied return: FCF yield [x%] + Growth [x%] = [x%] [source: C]
FCF conversion trend: [stable / deteriorating — cite years]
Market pricing signal: Optionality priced at near-zero? [Yes/No/Partial]
[name what is being discounted and why]
Ecosystem tailwinds: [structural tailwind | source]
Ecosystem headwinds: [structural headwind | source]
India overlays: [Promoter track record | RPT flag | Liquidity | Regulatory]

---

**5. CLASSIFICATION AND SIZING**

Classification: [Zone]
ROOTMO flag: Yes / No / Watch
Suggested position: [size range with rationale]
Classification risk: [single reclassification trigger]
Mistake flag check: [Value trap? Optionality oversized? Middle?]

---

**6. ONE-LINE VERDICT**

[Company] is [classification] — [reason], but [tension].
Monitor [trigger].

---

**COMPARISON: DATA vs. USER INPUT**

**Output A — Divergences** (Think harder about these)
[Data says X | User input says Y | Investigate: Z]

**Output B — Agreements** (Conviction builders)
[List briefly]

**Output C1 — Blind Spots** (In the data, not in your prior)
[The evidence surfaced X which your input did not address]

**Output C2 — Your Edge** (In your prior, not in the data)
[You flagged X — unverifiable from data but preserved as
potentially high-value signal. Weight it accordingly.]

---

**SOURCE ATTRIBUTION**

[A] Company sources: [key documents and years]
[B] Channel checks: [n checks | types: competitor/ex-emp/customer]
[B2] Secondary adv.: [Value Picker / AmbitionBox / Glassdoor]
[C] Screener PDF: [date of PDF]
[E] User Input: [source types | biases noted]
[W] Web search: [specific searches run]
[U] Unresolved: [sections with no reliable source]

Low-confidence sections: [name and explain why]

---

**SECTION 2: USER INPUT**

---

[Reproduce the User Input verbatim as submitted — all text,
source attributions, and stated biases. No interpretation added.
Preserved for audit trail and future reference.]

**Extracted signals:**

D1  Capital allocation:         [DO/Implied/Absent] [source] [finding]
D2  Intellectual honesty:       [DO/Implied/Absent] [source] [finding]
D3  Long-term anchor:           [DO/Implied/Absent] [source] [finding]
D4  Ecosystem orientation:      [DO/Implied/Absent] [source] [finding]
D5  Pricing philosophy:         [DO/Implied/Absent] [source] [finding]
D6  Feedback loop awareness:    [DO/Implied/Absent] [source] [finding]
D7  New S-curve articulation:   [DO/Implied/Absent] [source] [finding]
D8  Experimentation comfort:    [DO/Implied/Absent] [source] [finding]
D9  Resilience as Optionality base: [DO/Implied/Absent] [source] [finding]
D10 Overall conviction:         [DO/Implied/Absent] [source] [finding]

DO = Directly Observed | Implied = inferred | Absent = excluded

**Impression Assessment:**

Quality (D1-D3): [H/M/L | reliability: full/provisional/unreliable]
Resilience (D4-D6): [H/M/L | reliability]
Optionality (D7-D10): [H/M/L | reliability]
Implied classification: [zone from User Input alone]
Excluded dimensions: [list any Absent dimensions]
Bias flags: [list any holder or other bias noted]

---

**GLOSSARY** *(for readers new to this framework)*

**The five classification zones:**
- Gambling: S-curve uncertain; binary outcome; very small position or avoid
- Optional: S-curve forming; asymmetric upside; small tail position (0.5-2%)
- Resilient + Optional: clearly convex; long-duration growth; core position (3-5%)
- Value Trap: S-curve turning concave; appears cheap but outcomes widening; avoid
- ROOTMO: Resilient core + adjacency optionality priced at near-zero; maximum
  conviction position (3-5%+). See full definition above in the memo header.

**NZS (Non-Zero Sumness):** The principle that the best businesses create
significantly more value for their ecosystem than they capture for themselves.
As information transparency increases, extractive businesses become
increasingly vulnerable to disruption. High NZS = durable competitive position.

**S-curve:** The lifecycle curve of a product or business — early convex
growth, peak, then concave decline. Most money is made when the curve is
convex; most money is lost when it turns concave. The goal is to find
companies with very long convex periods, or companies stacking new S-curves.

**Source tags in this memo:**
[A] = company-controlled sources (ARs, transcripts, presentations)
[B] = primary channel checks (direct competitor/ex-employee/customer conversations)
[B2] = secondary adversarial sources (Value Picker, AmbitionBox, Glassdoor)
[C] = Screener.in PDF (authoritative financial data source)
[E] = User Input (management meeting, sell-side, investor conversations)
[W] = web search [U] = unresolved / no reliable source found

**Comparison outputs:**
Output A = where data and user input disagree — investigate these
Output B = where both independently agree — conviction builders
Output C1 = what the data found that the user's prior missed — blind spots
Output C2 = what the user flagged that no data source could surface — your edge

**About this skill:** Built on the NZS Capital Resilience & Optionality
framework by Brinton Johns and Brad Slingerlend (Complexity Investing,
2014). Adapted for Indian listed equity analysis with India-specific
overlays including promoter capital allocation assessment, RPT screening,
and smallcap liquidity framing. Feedback and improvement suggestions
welcome — this skill is a work in progress.

---

*Type 'export to Word' for a formatted Word document.
Note: this requires additional processing.*

---

## Step 6 — Word Export (On Trigger Only)

Triggered by: "export to Word", "generate Word doc", "create docx".

Read /mnt/skills/public/docx/SKILL.md before proceeding.

The Word document should be meaningfully richer than the markdown:
- Framework overview as a styled title block
- Sections with proper page breaks
- Financial data from Screener PDF as real formatted tables
- Classification badge as a styled callout box
- Comparison output as a structured table with visual distinction
- User Input in Section 2 with source labels visually distinct
- Glossary as a styled reference section
- NZS Capital attribution in document footer

---

## Notes on Intellectual Honesty

On source conflict: When [A] and [B/B2] contradict each other,
the contradiction is the most important finding in the memo.
Name it, explain both sides, state which you weight more and why.

On holder bias: Flag it visibly. Do not discount arithmetically.
The reader adjudicates — the skill's job is to make the bias visible,
not to pretend it can be precisely corrected.

On uncertainty: A dimension marked Absent is more useful than one
filled with a plausible-looking score from thin evidence. Confidence
ratings exist to be used, not inflated.

On prediction: Predictions should be broad — what will not change
in customer needs — rather than narrow — what will happen to next
year's margins. Narrow predictions anchoring large positions are
the most common source of portfolio destruction.
