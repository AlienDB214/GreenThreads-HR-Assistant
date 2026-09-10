# GreenThreads Denver — HR Synthesis Brief

*AI.205: AI Integration in Business I · Homework \#2: Document Intelligence Project · HR Function*

# Sources

| Source | Description |
| :---- | :---- |
| **Source 1** | Sales Associate Offer Letter — GreenThreads Denver (Cherry Creek North), dated June 12, 2026 |
| **Source 2** | GreenThreads Employee Handbook, Section 3 — Compensation & Hiring (v2026.1) |
| **Source 3** | Job Requisition & Posting: Sales Associate, Denver, posted May 16, 2026 |
| **Source 4** | GT\_HR\_Denver\_Applicants.csv — 148 applicants across 14 Denver roles |

# Executive Summary

GreenThreads' Employee Handbook requires that hourly retail staff be paid “at or above the local market median” for comparable roles. The Sales Associate offer — the role with the most open seats in Denver — pays 11.4% below the local market rate, the largest gap of any role in the store. Applicant data confirms this is not a hypothetical risk: it is the single most common reason candidates decline offers, and it compounds with a second, related failure: recruiting promised an August start date, but actual offers were not extended until a September 28 start, contributing directly to the second-most-common decline reason. As of this analysis, 6 of the 8 Sales Associate seats remain unfilled.

# 1\. What Each Document Actually Says

## Sales Associate Offer Letter

*“Rate of pay: $17.50 per hour... Proposed start date: September 28, 2026... This offer... remains open for five (5) business days.”*

## Employee Handbook, §3.1–§3.4

*“GreenThreads pays hourly retail staff at or above the local market median for comparable roles... a long gap between application and start date increases the risk that strong candidates accept other offers... A declining offer-accept rate is an early signal that pay or timing is out of step with the local market.”*

## Job Posting (May 16, 2026\)

*“Target start: August 2026, ahead of our fall opening — join us for training and help launch the store.”*

## 

## 

## Applicant Dataset — Sales Associate Role

88 applicants for 8 openings. Stage breakdown: 36 Applied, 26 Screened, 15 Interviewed, 9 Offers declined, 2 Offers accepted. Of the 9 declined offers: 5 cite “pay below expectations,” 3 cite “start date too far out,” 1 “accepted another offer.” 6 of 88 Sales Associate applicants have sat in the “Applied” stage 30+ days with no contact.

# 2\. The Pay Gap, By Role

| Role | Offered Rate | Denver Market Rate | % Below Market |
| :---- | :---- | :---- | :---- |
| **Store Manager** | $68,000 | $72,000 | 5.6% |
| **Assistant Manager** | $52,000 | $54,000 | 3.7% |
| **Sales Associate** | $17.50/hr | $19.75/hr | **11.4%** |
| **Stock Associate** | $18.00/hr | $18.50/hr | 2.7% |
| **Visual Merchandiser** | $22.00/hr | $22.50/hr | 2.2% |

*Sales Associate carries both the largest percentage gap below market and the most open seats (6 of 8\) — the role where the handbook's own pay policy is furthest from being followed.*

# 3\. Grounding — Every Key Claim Traced to Its Source

| Claim | Traced To (Exact Source) |
| :---- | :---- |
| Pay is 11.4% below market for Sales Associate | Applicant dataset: $17.50 offered vs. $19.75 Denver market rate, Sales Associate rows |
| Company policy requires at/above-market pay | Employee Handbook §3.1, direct quote |
| Posting promised August start; offer letter set September 28 | Job posting “Target start” line vs. offer letter “Proposed start date” line |
| Pay is the top reason for declined Sales Associate offers | Applicant dataset: 5 of 9 declined offers, Decline\_Reason field |
| Start date is the second most common decline reason | Applicant dataset: 3 of 9 declined offers, Decline\_Reason field |
| 6 of 8 Sales Associate seats remain open | Applicant dataset: Openings\_For\_Role (8) minus Offer\_Accepted \= Y count (2) |

# 4\. Cross-Source Synthesis

Three independent sources converge on one finding: GreenThreads is not following its own hiring policy, and its own data shows the measurable cost of that gap. The Handbook sets the rule (§3.1: pay at or above market). The applicant data shows the rule broken specifically for Sales Associate, by the largest margin of any role. And the decline reasons in that same dataset show candidates responding exactly as the Handbook itself predicts (§3.4 names a declining offer-accept rate as an early warning sign of pay or timing misalignment). This is not three separate findings — it is one finding confirmed three independent ways: policy, practice, and outcome all point the same direction.

A second thread compounds the first. A candidate who applied in May expecting an August start (per the job posting), then received a September 28 offer with only five business days to decide, was handed two reasons to walk away at once: below-market pay and a slipped timeline. This plausibly explains why “start date too far out” sits directly behind pay as the second most common decline reason.

# 5\. Actionable Insight for an HR Manager

The recommendation is not a vague call to “consider raising pay” — it is a specific, policy-grounded action: bring Sales Associate pay in line with GreenThreads' own written compensation standard, currently missed by 11.4%, because the applicant data shows this exact gap already accounts for over half of all declined offers on the role the store can least afford to leave short. Secondarily, recruiting communications should stop advertising an August start when actual offers are not extended until systems and staffing plans catch up — that mismatch is quietly costing qualified candidates as well.

*This connects directly to the HR function goal established in Homework \#1: reducing time-to-hire and protecting retention by closing the gap between what GreenThreads promises candidates and what it actually delivers.*

# Appendix: Prompts, Tools & Verification

## Prompts Used

| Prompt Used | Purpose / What Worked |
| :---- | :---- |
| "Extract every column in this dataset and state what it actually measures. Do not assume a column means what its name says." | Used to correctly identify that Openings\_For\_Role is a static target headcount, not a live remaining-seats count — prevented a 25% overstatement of open Sales Associate positions. |
| "Using only the applicant dataset, calculate: total Sales Associate applicants, stage breakdown, and decline reasons with counts." | Produced the exact figures used in Section 1 and 3 — verified independently against a second pass of the raw data before inclusion. |
| "Compare the pay rate in the offer letter against the Denver market rate in the dataset. Calculate percent difference for every role, not just Sales Associate." | Surfaced that Sales Associate has both the largest pay gap and the most open seats — not assumed, calculated across all five roles for comparison. |
| "Does anything in the Employee Handbook contradict the offer letter or the job posting? Quote the exact clause." | Surfaced the §3.1 compensation-policy conflict and the August-vs-September start date conflict — both grounded in exact quoted text, not inference. |

## Tools & Model Tiers

Analysis was conducted using Claude (Sonnet-tier) for document extraction, cross-source comparison, and calculation verification. A second pass was run on all numeric claims (decline reason counts, pay-gap percentages) by re-querying the raw dataset directly with pandas rather than relying on a single AI-generated summary, to catch any figures the model may have stated confidently without full grounding.

## Verification Method

Every quantitative claim in this brief was checked against the source file or document directly before inclusion. Two issues were caught and corrected during this process: (1) an early draft misread Openings\_For\_Role as a live open-seat count rather than a static target, which would have overstated Sales Associate hiring need by 25%; (2) the September 28 opening date referenced in earlier team drafts required verification against the confirmed source set before being trusted, since it initially appeared only in a secondary summary document rather than an official source.

## Data Governance Consideration

The applicant dataset contains real names, pay rates, and personal decline reasons for 148 individuals — this is sensitive HR data. Per the case brief, GreenThreads currently has no formal AI usage policy, despite holding real employee and candidate data. Recommendation: applicant-level data (individual rows, names, or exact pay figures) should not be entered into a public, consumer-facing AI tool without redaction or an approved enterprise AI environment. Aggregate findings (percentages, category counts, as used throughout this brief) are lower-risk and appropriate to share more broadly, but the underlying raw file should be treated as confidential HR data until GreenThreads establishes a formal AI governance policy.

