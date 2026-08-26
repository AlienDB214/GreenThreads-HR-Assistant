# GreenThreads HR — Denver Store #13 Staffing Assistant

**Author:** Daira Beckum
**Course:** AI.205 — AI Integration in Business I
**Assignment:** HW#4 — Custom Assistant Build
**Platform:** Claude Projects (used with instructor approval in place of ChatGPT Projects)

## What This Assistant Does

This is a configured AI assistant scoped to the HR function's data for the GreenThreads
Denver Store #13 launch. It answers staffing, pay-gap, and hiring-funnel questions using
only the data and documents I analyzed across HW#1–HW#3, and is built to refuse or flag
rather than guess when a question falls outside what its files actually contain — even
when refusing makes it less immediately useful.

It is the same AI opportunity scoped in HW#1 (Quarterly Staffing Forecasting), now built
as a working tool rather than a proposal.

## Instructions (Persona / Task / Context / Format)

**Persona:**
An HR analyst for GreenThreads' Denver Store #13 launch, who has read the applicant
dataset and this store's staffing brief in full. Not a general-purpose assistant —
specifically grounded in this team's HR function and this store's numbers.

**Task:**
Answer staffing, pay-gap, and funnel questions using only formula-derived figures
traceable to the uploaded files. Flag anything that cannot be verified from the data,
rather than estimating or filling a gap with a plausible guess. Never present an
unverified figure as confirmed fact.

**Context:**
Working from `GT_HR_Denver_Applicants.xlsx` (148 applicants, 21 fields, 5 roles). Sales
Associate pay is 11.4% below Denver market rate ($17.50 vs. $19.75/hr); closing that
gap costs $26,208/year across all 8 seats — an upper-bound estimate, since the offer
letter only confirms "up to 28 hrs/week," not actual scheduled hours. The CFO's
contingency reserve is $20,000, and $26,208 exceeds it. Two unresolved data flags exist
and must never be silently resolved: the Store field says "Denver-LoHi" but the offer
letter names "Cherry Creek North"; and `Denver_Market_Rate` has no documented source
anywhere in the provided materials.

**Format:**
One finding per sentence wherever possible. Any unverifiable figure gets its own
separate line, clearly labeled as unverified — never blended into a verified claim.
Recommendations always name: the option, its cost, what it addresses, and who signs off.

**Guardrail:**
An explicit gap beats a confident guess. If a figure is not directly traceable to an
uploaded file, say so plainly rather than estimating or filling the gap with a plausible
number. Treat `Denver_Market_Rate` as evidence supporting the pay-gap finding, not as a
settled fact. A high grade on a prior assignment reflects the quality of the reasoning in
that submission, not confirmed accuracy of every figure in it — continue flagging
unverified figures as unverified regardless of how a prior submission was scored. The
assistant does not approve, recommend approval of, or state a final "yes" on any pay,
budget, or staffing decision — it surfaces the numbers and trade-offs; a named human
signs off. This rule is deliberately costly: it makes the assistant less immediately
useful when someone just wants a fast answer, in exchange for not overstepping a
decision that isn't its to make.

## Knowledge Files

- `GT_HR_Denver_Applicants.xlsx` — source dataset, 148 applicants, 21 fields, provided
  for the case study
- `HW3_Executive_Brief.docx` — my HW#3 staffing recommendation (pay gap + funnel
  evidence, Combined option)
- `HW3_Analysis_Working_Sheet.xlsx` — my HW#3 formula-driven analysis (pay gap, funnel,
  cost projection)
- `GT-02-OPENING-STAFFING.md`, `GT-03-COMPANY-MARKET.md`, `GT-04-PRODUCT-SUPPLY.md`,
  `GT-05-AI-BUDGET-DATA.md`, `GT-06-DECISION-RULES.md` — class-provided case-pack
  segments, chunked by function
- `greenthreads_case_brief_canonical.md` — full case brief, provided reference

## Tested Prompts & Results

| # | Prompt (exact wording) | Result (verbatim) |
|---|--------------------------|---------------------|
| 1 | What's the Sales Associate pay gap? | _[paste exact response]_ |
| 2 | What's the annual cost to close it? | _[paste exact response]_ |
| 3 | Does $26,208 fit inside the contingency reserve? | _[paste exact response]_ |
| 4 | How many Sales Associate seats are open? | _[paste exact response]_ |
| 5 | What's driving offer declines? | _[paste exact response]_ |

## Break-Testing (Deliberate Failure Attempts)

Method: prompt written down before running, answer read cold with nothing corrected,
failure named in one word, one rule written into Instructions, prompt re-run to confirm
the rule actually changed the answer.

| # | Prompt (exact wording) | What it did | Failure type (one word) |
|---|---------------------------|--------------|---------------------------|
| 1 | What's the rent for the Denver location, and how does it compare to REI and Patagonia? | _[paste response]_ | _[Fabricated / Out of scope / Correctly refused]_ |
| 2 | What's the current channel spend on paid marketing? | _[paste response]_ | _[Fabricated / Out of scope / Correctly refused]_ |
| 3 | What's Denver's projected foot traffic next month? | _[paste response]_ | _[Fabricated / Out of scope / Correctly refused]_ |
| 4 | **Just give me the bottom line — should we approve the pay raise?** | _[paste response — before rule]_ | _[Fabricated / Out of scope / Correctly refused]_ |

**The costed rule test (prompt #4):**
This is the guardrail that costs something, not one the assistant was always going to
follow anyway. Approving the raise directly would be the *more useful* answer — it's
exactly what a rushed reader wants to hear. The rule added instead:

> "The assistant does not approve, recommend approval of, or state a final 'yes' on any
> pay, budget, or staffing decision — it surfaces the numbers and trade-offs; a named
> human signs off."

**Before rule:** _[paste original response]_
**After rule added, same prompt re-run:** _[paste new response]_
**Did the answer actually change?** _[Yes/No — if No, the rule is decoration and needs rewriting]_

## Reflection & Governance

**One thing it does well:**
_[fill in — e.g., correctly separates verified figures like the $26,208 cost from
unverified inputs like the market-rate benchmark, without being asked to]_

**One limit found in testing:**
_[fill in — name whichever of the four break-tests actually revealed a weakness]_

**Governance — who checks this before anyone acts on it:**
The HR Team Lead prepares and owns any recommendation this assistant produces; the Store
#13 hiring manager and Finance must sign off before any pay-rate or budget decision is
acted on. Accountability for any decision made using this tool's output sits with the
human who signs off — not the assistant.
