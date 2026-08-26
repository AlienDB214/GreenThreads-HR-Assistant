---
chunk_id: GT-05-AI-BUDGET-DATA
parent_document_id: GT-CASE-BRIEF
title: "AI Maturity, Governance, Budget, Targets, and Data Assets"
document_type: semantic_retrieval_chunk
authority: instructor_provided
content_status: authoritative_case_context
source_pages: [3, 4, 5]
topics:
  - AI maturity
  - AI policy
  - data governance
  - customer data
  - employee data
  - Denver budget
  - revenue target
  - team datasets
applies_to: [All, Operations, Finance, Marketing A, Marketing B, HR]
related_chunks: [GT-01-ENGAGEMENT, GT-02-OPENING-STAFFING, GT-04-PRODUCT-SUPPLY, GT-06-DECISION-RULES]
retrieval_queries:
  - "How is GreenThreads using AI today?"
  - "What is the AI governance gap?"
  - "What is Denver's opening budget?"
  - "Which dataset belongs to each team?"
  - "What is Denver's revenue target?"
---

# GT-05 - AI Maturity, Governance, Budget, Targets, and Data Assets

## Current AI Maturity

GreenThreads is doing almost nothing with AI. A few people use ChatGPT unofficially. Nothing is built into a workflow. The company has an IT team but no data or analytics function. Reporting is ad hoc, and it is somebody's Friday afternoon.

## Governance Gap

GreenThreads has no AI policy. Nobody has said what can be fed to a public tool, and the company holds real customer data and real employee data. The absence of a policy is not permission. This is the gap the team's guardrail must close.

## Denver Opening Budget

| Line | Amount |
|---|---:|
| Buildout & fixtures | $150,000 |
| Opening inventory | $110,000 |
| Marketing & launch | $85,000 |
| Staffing & recruiting | $65,000 |
| Tech & systems | $20,000 |
| Contingency | $20,000 |
| **Total** | **$450,000** |

## Performance Reference and Target

- Austin launched on $350K and generated approximately $1.67M in year one.
- Denver's target is approximately $2.1M.

## Available Data

Each team gets a dataset. It is real enough to be wrong in interesting ways. Check it before trusting it.

| Team | File | Description |
|---|---|---|
| All | `GT_SKU_Catalog.csv` | 8 SKUs, suppliers, lead times, costs, order deadlines |
| Operations | `GT_Ops_Inbound_Shipments.csv` | 96 POs over 180 days, promised vs. actual |
| Finance | `GT_Finance_Denver_Budget.csv` | Denver budget data |
| Finance | `GT_Finance_Spend_Transactions.csv` | Denver spend transactions |
| Finance | `GT_Finance_Austin_Store_Daily.csv` | Austin store daily data |
| Marketing A | `GT_MarketingA_Channel_Performance.csv` | Austin launch, 30 days x 4 channels |
| Marketing B | `GT_MarketingB_Customers.csv` | 280 customers, orders and spend |
| HR | `GT_HR_Denver_Applicants.csv` | 148 applicants for 14 Denver roles |

## Data-Use Rule

Use the datasets as evidence, but validate them before analysis. Dataset contents should not silently overwrite the case brief's fixed facts.

