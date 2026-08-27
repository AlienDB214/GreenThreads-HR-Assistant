GREENTHREADS — DENVER STORE \#13

**Sales Associate Staffing Recommendation**

*HR Function  •  Daira Beckum  •  HW3 Data Intelligence Project*

**EXECUTIVE SUMMARY**

This extends the Quarterly Staffing Forecasting opportunity identified in HW1. Sales Associate pay sits 11.4% below the Denver market rate ($17.50 vs. $19.75/hr) — the largest gap of any role and the \#1 stated reason candidates decline offers (5 of 9 declines). Independent behavioral evidence corroborates this: 6 of 88 Sales Associate applicants have gone stale (30+ days, no contact) before a pay decision is ever reached, and the average offer-to-decision window runs 6.2 days. Six of eight open Sales Associate seats remain unfilled. Closing the gap costs $26,208/year across all 8 seats.

**KEY FINDINGS**

•  Pay gap: 11.4% below market, largest of any role

•  Pay \= \#1 decline reason (5 of 9 declines)

•  6 of 88 applicants stale before decision

•  6.2-day avg. offer-to-decision window

•  6 of 8 seats remain open

![][image1]

**CHOICE SET & RECOMMENDATION**

| Option | Annual Cost | Addresses |
| :---- | :---- | :---- |
| 1\. Raise pay to market | $26,208 | Pay decline reason only |
| 2\. Automate stale-applicant follow-up | $0\* | Contact gap only |
| **3\. Both (recommended)** | **$26,208** | **Both named decline reasons \+ behavioral evidence** |

*\*Assumes automation via existing HR tools; no new licensing cost identified in current dataset. Cost figures assume the full 28 hrs/week ceiling stated in the offer letter ("up to 28 hrs/week") — actual scheduled hours are not confirmed in the data, so $26,208 is an upper-bound estimate, not a confirmed cost.*

**Recommendation:** Pursue Option 3\. Raise Sales Associate pay to $19.75/hr to match market rate, and automate stale-applicant follow-up so candidates don't disengage before pay ever becomes the deciding factor. Two independent evidence lines — exit-survey decline reasons and funnel behavior — point to the same root cause and the same fix.

**DECISION RIGHTS & GOVERNANCE**

The HR Team Lead prepares and owns this recommendation; final pay-rate approval requires sign-off from the Store \#13 hiring manager and Finance, given budget impact. A human reviews and approves any stale-applicant follow-up before it sends — automation flags candidates; it does not contact them unprompted.

**Tools, Method & Verification**

**DATA SOURCE**

GT\_HR\_Denver\_Applicants.xlsx — 148 applicants, 21 fields, provided dataset. Sales Associate subset (n=88) analyzed for this brief.

**CLEANING & VALIDATION**

12-point check run against the full dataset: no duplicate IDs, no duplicate rows, no negative/impossible day values, no whitespace/casing inconsistencies, no logical contradictions between offer/decision fields and current stage. Structural nulls in stage-timing columns confirmed as expected (candidate has not yet reached that stage), not data errors.

Three flags carried forward rather than silently resolved: (1) all 148 rows list Store as "Denver-LoHi," which does not match "Cherry Creek North" named in the sourced offer letter — unresolved discrepancy. (2) Denver\_Market\_Rate has no documented source anywhere in the provided materials; the entire pay-gap finding rests on this unverified benchmark. (3) The offer letter states "up to 28 hrs/week" — a ceiling, not a confirmed scheduled amount — so the $26,208 annual cost figure is an upper-bound estimate, not a confirmed cost.

**ANALYSIS & VERIFICATION**

All figures are formula-driven (AVERAGE, COUNTIF, COUNTIFS) in the linked working sheet — no hand-typed results. Every formula was recalculated and checked for errors before use.

Verification catch: an early version of the annual-cost formula referenced the wrong cell (percentage gap instead of dollar gap), returning $165/seat instead of the correct $3,276/seat. Caught by independently re-deriving the figure by hand and comparing it against the formula output before the number was used anywhere downstream — the same "prove one number" check applied to my own work, not just the source data.

**SUPPORTING SHEET**

**\[INSERT GOOGLE SHEET LINK HERE\]**  


[image1]: <data:image/png;base64,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>