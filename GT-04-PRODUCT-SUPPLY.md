---
chunk_id: GT-04-PRODUCT-SUPPLY
parent_document_id: GT-CASE-BRIEF
title: "Denver Products, Inventory, and Supply-Chain Constraints"
document_type: semantic_retrieval_chunk
authority: instructor_provided
content_status: authoritative_case_context
source_pages: [3]
topics:
  - Denver launch assortment
  - SKUs
  - inventory
  - suppliers
  - lead times
  - order deadlines
  - Vietnam
  - typhoon risk
applies_to: [All, Operations, Finance]
related_chunks: [GT-03-COMPANY-MARKET, GT-05-AI-BUDGET-DATA, GT-06-DECISION-RULES]
retrieval_queries:
  - "Which products launch in Denver?"
  - "When must Bamboo Joggers be ordered?"
  - "What is the opening inventory buy?"
  - "What supply-chain risks affect Denver?"
---

# GT-04 - Denver Products, Inventory, and Supply-Chain Constraints

## Denver Launch Assortment

GreenThreads sells eight SKUs across its 12 stores. Denver launches with four of them.

| Product | Supplier | Country | Lead time | MOQ | Cost | MSRP | Margin |
|---|---|---|---:|---:|---:|---:|---:|
| Classic Tee | Delta Organics | India | 45 days | 500 | $14.25 | $38 | 62.5% |
| Active Shorts | Mekong Textile Co. | Vietnam | 60 days | 300 | $22.00 | $58 | 62.1% |
| Bamboo Joggers | Song Hong Apparel | Vietnam | 65 days | 250 | $30.00 | $78 | 61.5% |
| EcoFleece Hoodie | Andes Knitworks | Colombia | 30 days | 200 | $38.00 | $98 | 61.2% |

SKU costs, MSRPs, lead times, MOQs, and suppliers as listed are fixed facts.

## Catalog-Only Products

The other four products are:

- Performance Polo
- Organic Tank Top
- Slim Chino
- Recycled Denim Jacket

They are in the GreenThreads catalog and stocked at other stores, but they are **not in the Denver launch assortment**. Don't plan around them, don't budget for them, and don't market them. They are marked `In_Denver_Launch = N` in the SKU catalog.

## Opening Inventory

Four SKUs, not eight, is a deliberate client decision. Fewer SKUs mean deeper stock on each product and fewer supplier relationships to manage against a 90-day clock.

The full opening buy is:

- $110,000 at cost.
- $287,800 at retail.
- All four Denver launch SKUs.
- Roughly six weeks of stock.

## Timing Constraint

The Bamboo Joggers have a 65-day lead time. With 90 days until opening, that order must be placed within the next 25 days or Denver opens with empty shelves. That assumes the supplier hits its promised date; use the inbound shipments data to test whether suppliers do.

## Supply-Chain Risk

Two of the four Denver launch products come from Vietnam. Together, they represent $54,900 of the $110,000 opening inventory buy. There is an active typhoon-season risk on that shipping lane, and nobody has hedged it.

