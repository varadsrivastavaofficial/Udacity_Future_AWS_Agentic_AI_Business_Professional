from pathlib import Path

report = """# NovaTech Solutions — Revenue Intelligence Report

**Prepared for:** Sarah Chen, VP  
**Prepared by:** Varad Srivastava  
**Date:** 13 September 2026

## 1. Executive Overview

The Revenue Intelligence dashboard brings together NovaTech's marketing, sales, and customer-support information into three interactive views: **Marketing Funnel**, **Sales Pipeline**, and **Customer Health**. The dashboard is designed to support management decisions around marketing efficiency, sales performance, and customer health.

The analysis combines a unified account-level dataset with the raw Marketing and Support datasets where campaign- or ticket-level detail is required. Quick Chat (Q) complements the dashboard by allowing natural-language questions and ad-hoc exploration.

## 2. Data Strategy

The CRM dataset contains **499 opportunities**, including **315 Won** and **184 Lost** outcomes. The Marketing dataset contains **2,240 leads**, including **609 responses**, giving an overall response rate of approximately **27.2%**. The Support dataset contains **3,000 tickets**.

Marketing and Support data were aggregated by `account_id` to create account-level measures. Marketing aggregation produced lead count, total campaign spend, and total marketing revenue. Support aggregation produced support-ticket count and average resolution time.

The CRM data was enhanced with calculated fields for **Won Deal Revenue** and **High Value Deal Flag**. The resulting account-level information was joined using `account_id`.

The raw Marketing and Support datasets were also retained in the analysis. This was important because aggregation can remove detailed dimensions such as campaign channel, funnel stage, ticket priority, product area, and customer sentiment. Retaining the raw datasets allowed these dimensions to be analysed directly in the dashboard.

## 3. Dashboard Design Rationale

### Marketing Funnel

The Marketing Funnel focuses on campaign engagement, lead progression, revenue attribution, and spending efficiency. It includes total campaign spend, response rate by channel, revenue by channel, funnel-stage distribution, campaign return on investment (ROI), and spend versus attributed revenue.

This view allows management to identify high-response channels and campaigns where expenditure may not be generating sufficient attributed revenue.

### Sales Pipeline

The Sales Pipeline focuses on deal outcomes, revenue, product performance, loss reasons, closing time, and company-size performance. It includes total deal revenue, Won versus Lost opportunities, average deal value by company size, revenue by product, loss reasons, regional performance, days to close, and win-rate analysis.

A **key performance indicator (KPI)** is a summary measure used to monitor an important business outcome. The Sales Pipeline uses KPI cards and supporting visuals to provide a concise view of sales performance.

### Customer Health

The Customer Health view focuses on support demand, resolution efficiency, product-area issues, customer sentiment, and account-level risk indicators. It includes total ticket volume, average resolution time by priority, support tickets by product area, sentiment distribution, and account-level support and commercial information.

The combination of support activity and commercial information is intended to help identify accounts that may require proactive attention.

## 4. Key Insights and Recommended Actions

### Sales Pipeline

- NovaPulse Professional has the highest total deal value at **$208,724**, while NovaEdge Lite has **$3,251**.
- Enterprise companies have the highest average deal value at **$1,589.17**, compared with **$1,353.30** for Medium companies.
- NovaPulse Ultimate has the longest average closing time at **99.5 days**, compared with **60.42 days** for NovaPulse Professional.
- Budget Constraints is the least common loss reason with **31 occurrences**, followed by Timing Not Right with **33**.

**Recommended action:** Prioritise high-value Enterprise opportunities and investigate the longer sales cycle for NovaPulse Ultimate to identify potential process or product-related delays.

### Customer Health

- YieldMax Software has the highest support volume at **334 tickets**, compared with **180** for TrueNorth Electronics.
- Average resolution time is relatively similar across priorities: **1.97 days for Low**, **1.92 days for High**, **1.92 days for Medium**, and **1.79 days for Critical**.
- Notifications is the most ticket-heavy product area with **601 tickets**, while Data Pipeline has **310**.
- Customer sentiment is predominantly neutral (**1,953 tickets**). Negative sentiment (**684**) is more than twice positive sentiment (**304**).

**Recommended action:** Investigate recurring issues affecting high-ticket-volume accounts and prioritise the Notifications product area for root-cause analysis. Negative sentiment should also be considered when identifying accounts requiring proactive engagement.

### Marketing Funnel

- Direct Mail has the highest campaign response rate at **53.02%**.
- Partner Referral contributes **$676,976.95** of attributed revenue out of **$1,127,223.09** and generates **807 of the 2,240 leads**.
- Total campaign spend is **$12,359,497.34**.
- NovaPulse Launch is the highest revenue-generating campaign at **$394,156.59**, while Digital Retarget has the highest spend at **$2,423,781.95**.
- All campaign channels show negative ROI, with Direct Mail performing best at **-70.74%**.

**Recommended action:** Analyse why Direct Mail and Partner Referral generate stronger engagement or revenue contribution, while reviewing high-spend and negative-return campaigns for optimisation and possible budget reallocation.

## 5. Quick Chat and Topic Configuration

Quick Chat was used to explore the data using natural-language questions. A **Topic** is the semantic layer that provides Q with the data fields and business context it can use to interpret questions.

The initial Topic configuration relied on the unified account-level dataset. This worked well for questions based on account-level measures, but it limited questions requiring fields that had been removed through aggregation. In particular, campaign-channel conversion and ticket-priority resolution questions were initially difficult because fields such as `campaign_channel` and `priority` were not available at the required level of detail.

After Topic configuration and the availability of the relevant datasets, Q was able to answer the exploration questions more effectively. For example, Q identified Direct Mail as the highest-converting channel at **53.02%**, reported the average deal values by company size, and identified YieldMax Software as the highest-support-volume account.

The Q exploration also highlighted the importance of validating AI-generated answers against the dashboard. For the top-account question, Q correctly identified YieldMax Software's **334 support tickets**, but its reported won-deal revenue of **$40,722** differed from the dashboard's **$25,791**. This is recorded as a partial match rather than treating the AI output as automatically correct.

## 6. AI Analysis vs. Dashboard

Q and the dashboard generally agreed on findings that could be directly supported by the relevant fields and aggregations. The dashboard provides a structured and repeatable way to monitor KPIs, compare categories, apply filters, and communicate findings visually.

Q is more useful for rapid, natural-language exploration and ad-hoc questions. The dashboard is more appropriate for recurring management reporting and visual decision-making.

The difference in the YieldMax deal-revenue result demonstrates why AI analysis should be cross-checked against the underlying dashboard. Q can accelerate investigation, but dashboard and dataset validation remains important when an answer depends on aggregation or joins.

## 7. Conclusion

The Revenue Intelligence dashboard provides a consolidated management view of NovaTech's marketing efficiency, sales pipeline, and customer health. The combination of interactive dashboards, Quick Chat, Topic configuration, and data validation supports both recurring management reporting and flexible business-question exploration.

The main opportunities identified are to improve marketing-spend efficiency, investigate high-support-volume accounts and product areas, and focus sales attention on higher-value opportunities while examining longer sales cycles.
"""

path = Path("/mnt/data/NovaTech_VP_Sarah_Chen_Final_Report.md")
path.write_text(report, encoding="utf-8")
print(path)
