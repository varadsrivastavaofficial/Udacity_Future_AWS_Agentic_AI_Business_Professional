# NovaTech Solutions — Revenue Intelligence Report

**Prepared for:** Sarah Chen, VP  
**Prepared by:** Varad Srivastava  
**Date:** 13 September 2026

## 1. Executive Overview

The Revenue Intelligence dashboard brings together NovaTech's marketing, sales, and customer-support information into three interactive views: **Marketing Funnel**, **Sales Pipeline**, and **Customer Health**. The dashboard supports management decisions around marketing efficiency, sales performance, and customer health.

The analysis combines a unified account-level dataset with the raw Marketing and Support datasets where campaign- or ticket-level detail is required. **Customer relationship management (CRM)** data records sales opportunities and their outcomes. Quick Chat (Q) complements the dashboard through natural-language questions and ad-hoc exploration.

## 2. Data Strategy

The CRM dataset contains **499 opportunities**, including **315 Won** and **184 Lost** outcomes. The Marketing dataset contains **2,240 leads**, including **609 responses**, giving an overall response rate of approximately **27.2%**. The Support dataset contains **3,000 tickets**.

Marketing and Support data were aggregated by `account_id` to create account-level measures. **Account-level aggregation** means combining multiple records belonging to the same customer account into summary measures for that account. `account_id` is the business identifier used to recognise the same customer account across the source datasets and connect its sales, marketing, and support information.

The CRM data was enhanced with calculated fields for **Won Deal Revenue** and **High Value Deal Flag**. The resulting information was joined using `account_id`.

**Granularity and account coverage:** The CRM dataset is opportunity-level, meaning each record represents a sales opportunity. Marketing and Support are more granular, with individual lead and ticket records. The unified dataset is anchored on CRM accounts through a left join, so its account-level totals represent accounts matched to the CRM population. Marketing and Support records belonging to orphan account IDs that do not appear in CRM are therefore excluded from the unified joined dataset, although the raw Marketing and Support datasets retain those records for detailed analysis. Consequently, unified-dataset totals should not be interpreted as totals for every account appearing in the raw source files.

The raw Marketing and Support datasets were also retained because aggregation can remove detailed dimensions such as campaign channel, funnel stage, ticket priority, product area, and customer sentiment.

## 3. Dashboard Design Rationale

### Marketing Funnel

The Marketing Funnel focuses on campaign engagement, lead progression, revenue attribution, spending efficiency, campaign return on investment (ROI), and spend versus attributed revenue.

### Sales Pipeline

The Sales Pipeline focuses on deal outcomes, revenue, product performance, loss reasons, closing time, and company-size performance. A **key performance indicator (KPI)** is a summary measure used to monitor an important business outcome.

### Customer Health

The Customer Health view focuses on support demand, resolution efficiency, product-area issues, customer sentiment, and account-level risk indicators. The combination of support activity and commercial information helps identify accounts that may require proactive attention.

## 4. Key Insights and Recommended Actions

### Sales Pipeline

- NovaPulse Professional has the highest total deal value at **$208,724**, while NovaEdge Lite has **$3,251**.
- Enterprise companies have the highest average deal value at **$1,589.17**, compared with **$1,353.30** for Medium companies.
- NovaPulse Ultimate has the longest average closing time at **99.5 days**, compared with **60.42 days** for NovaPulse Professional.
- Budget Constraints accounts for **31** loss occurrences, while Timing Not Right accounts for **33**.

**Recommended action:** Prioritise high-value Enterprise opportunities and investigate the longer sales cycle for NovaPulse Ultimate.

### Customer Health

- YieldMax Software has the highest support volume at **334 tickets**, compared with **180** for TrueNorth Electronics.
- Average resolution time is **1.97 days for Low**, **1.92 days for High**, **1.92 days for Medium**, and **1.79 days for Critical**.
- Notifications is the most ticket-heavy product area with **601 tickets**, while Data Pipeline has **310**.
- Customer sentiment is predominantly neutral (**1,953 tickets**); negative sentiment is **684**, compared with **304 positive**.

**Recommended action:** Investigate recurring issues affecting high-ticket-volume accounts and prioritise the Notifications product area for root-cause analysis.

### Marketing Funnel

- Direct Mail has the highest campaign response rate at **53.02%**.
- Partner Referral contributes **$676,976.95** of attributed revenue out of **$1,127,223.09** and generates **807 of the 2,240 leads**.
- Total campaign spend is **$12,359,497.34**.
- NovaPulse Launch generates **$394,156.59**, while Digital Retarget has **$2,423,781.95** of spend.
- All campaign channels show negative ROI, with Direct Mail performing best at **-70.74%**.

**Recommended action:** Review high-spend negative-return campaigns and investigate the characteristics behind stronger engagement and revenue contribution.

## 5. Quick Chat and Topic Configuration

Quick Chat was used to explore the data using natural-language questions. A **Topic** is the semantic layer that provides Q with selected data fields and business context.

The saved Topic, **NovaTech Revenue Intelligence**, contains the unified account-level dataset. It supports account-level questions such as deal counts, average deal value by company size, total support tickets, marketing spend, and account-level support volume.

The account-level Topic has an important limitation: dimensions removed through aggregation, such as campaign channel and ticket priority, are not available for every question. Raw Marketing and Support datasets remain necessary for detailed campaign-channel and ticket-priority analyses.

Fresh Topic testing confirmed answers such as **499 CRM deals** and the average deal values by company size, which were cross-checked against the dashboard.

## 6. AI Analysis vs. Dashboard

Q and the dashboard generally agreed when the relevant fields, metric definitions, and aggregation levels matched. Q is useful for rapid natural-language exploration, while the dashboard is better for repeatable KPI monitoring, filtering, visual comparison, and management reporting.

For the top-account question, Q correctly identified YieldMax Software with **334 support tickets**, but reported **$40,722** in won-deal revenue versus **$25,791** in the dashboard's account-level value. This is a **partial match**. The difference should be validated against opportunity-level CRM records before use in a financial decision.

There was also a metric-definition issue in the marketing question. Q described Direct Mail's **53.0%** result as a conversion rate, while the matching dashboard visual measures **campaign response rate** and shows **53.02%**. The numerical value agrees, but the terminology is not equivalent without a defined conversion event.

## 7. Conclusion

The Revenue Intelligence dashboard provides a consolidated management view of NovaTech's marketing efficiency, sales pipeline, and customer health. The combination of interactive dashboards, Quick Chat, Topic configuration, and explicit validation supports both recurring management reporting and flexible business-question exploration.

The main opportunities are to improve marketing-spend efficiency, investigate high-support-volume accounts and product areas, and focus sales attention on higher-value opportunities while examining longer sales cycles.
