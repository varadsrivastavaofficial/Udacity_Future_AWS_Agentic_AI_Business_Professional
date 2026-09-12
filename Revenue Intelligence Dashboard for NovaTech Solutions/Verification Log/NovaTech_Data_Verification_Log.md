# NovaTech Data Verification Log

**Student Name:** Varad Srivastava  
**Date:** 12 September 2026

## Verification Log

| # | Knowledge Base | Question Asked | Expected Answer | Q's Actual Answer | Match? | Notes |
|---|---|---|---|---|---|---|
| 1 | NovaTech CRM Deals | How many deals are in the CRM? | 499 | 499 | Yes | Q matched the CRM dataset count. |
| 2 | NovaTech CRM Deals | How many deals were won and lost? | 315 Won; 184 Lost | 315 Won; 184 Lost | Yes | Q matched the deal outcome counts. |
| 3 | NovaTech Marketing Campaigns | How many marketing leads are there? | 2,240 | 2,240 | Yes | Q matched the marketing dataset row/lead count. |
| 4 | NovaTech Marketing Campaigns | How many leads responded, and what is the overall response rate? | 609 responded; 27.2% response rate | 609 responded; 27.19% response rate | Yes | 27.19% rounds to 27.2%. |
| 5 | NovaTech Support Tickets | How many support tickets are there? | 3,000 | 3,000 | Yes | Q matched the support ticket count. |
| 6 | NovaTech Support Tickets | How many tickets are there by priority? | Critical 50; High 400; Medium 1,050; Low 1,500 | Critical 50; High 400; Medium 1,050; Low 1,500 | Yes | Q matched all four priority counts. |

## Cross-Check

- **Fact verified:** Total number of CRM deals.
- **Chat said:** 499 deals.
- **QuickSight shows:** 499 CRM deal records.
- **Consistent?** Yes.

## Data Quality Notes

The three structured datasets use `account_id` as the common account-level key. The source data also contains orphan account IDs in the Marketing and Support datasets; these were retained during preparation rather than silently removed. The final analysis uses the unified account-level dataset together with the raw Marketing and Support datasets where ticket- or campaign-level fields are required.
