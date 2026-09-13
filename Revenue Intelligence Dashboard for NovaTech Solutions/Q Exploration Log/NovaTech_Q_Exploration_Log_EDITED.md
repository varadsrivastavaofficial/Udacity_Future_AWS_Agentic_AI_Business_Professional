# NovaTech Q Exploration Log

**Student Name:** Varad Srivastava  
**Date:** 12 September 2026

## Q Exploration Questions

| # | Question Asked | Q's Answer (summarize) | Dashboard Visual Used to Cross-Check | Dashboard Shows | Match? | Notes |
|---|---|---|---|---|---|---|
| 1 | Which campaign channel has the highest conversion rate? | Q identified Direct Mail as having the highest rate at approximately 53.0%. | Marketing Funnel — Average of Campaign_response by Campaign_channel | Direct Mail has the highest **campaign response rate at 53.02%**. | Partial | The numerical result agrees with the dashboard, but the metric terminology differs. The dashboard measures **campaign response rate**, meaning the proportion of campaign records with a response, rather than a separately defined conversion rate. Therefore, Q's 53.0% answer matches the dashboard's response-rate value, but the term “conversion rate” should not be treated as identical without a defined conversion event. |
| 2 | What is the average deal size by company size? | Enterprise $1,589.17; Small $1,486.49; Medium $1,353.30; Large $1,257.47. | Sales Pipeline — Average Deal Value by Company Size | Enterprise $1,589.17; Small $1,486.49; Medium $1,353.30; Large $1,257.47. | Yes | Q and the dashboard agree on both the values and the ranking by company size. |
| 3 | What is the average resolution time for critical vs. low-priority tickets? | Critical: 1.79 days; Low: 1.97 days. | Customer Health — Resolution Time by Priority | Critical: 1.79 days; Low: 1.97 days. | Yes | Q and the dashboard agree; low-priority tickets take slightly longer on average than critical tickets. |
| 4 | What are the top 10 accounts by support ticket volume, and what is their total deal revenue? | YieldMax Software ranked highest with 334 support tickets and $40,722 in total won deal revenue. | Customer Health — At-Risk Accounts table | YieldMax Software has 334 support tickets and $25,791 in Won Deal Revenue. | Partial | Q correctly identified YieldMax Software as the highest-ticket-volume account, but its reported deal-revenue figure ($40,722) differs from the dashboard's $25,791. This indicates an aggregation/calculation difference that should be reviewed before using the figure for financial decisions. |
| 5 | Are there any campaigns where we spent more than we earned back? | Yes. Q identified 6 campaigns where campaign spend exceeded attributed revenue. | Marketing Funnel — Campaign Spend and Revenue Attributed by Campaign Name table | All 6 campaigns have campaign spend greater than attributed revenue: Digital Retarget ($2,423,781.95 vs. $196,249.17); Enterprise Expansion ($2,114,968.95 vs. $194,356.76); NovaEdge Awareness ($1,518,785.09 vs. $34,279.64); NovaPulse Launch ($2,423,202.47 vs. $394,156.59); Q3 Growth Sprint ($1,984,711.38 vs. $133,415.20); Year-End Accelerator ($1,894,047.50 vs. $174,765.73). | Yes | The dashboard table confirms the Q result using the actual numerical values rather than comparing bar and line heights on different axes. All six campaigns have spend greater than attributed revenue. |

## Reflection

### Where did Q agree with the dashboard?

Q agreed with the dashboard on the numerical findings that could be directly cross-checked. The average deal value by company size and resolution time by priority matched exactly. Q also correctly identified YieldMax Software as the account with the highest support ticket volume and correctly identified six campaigns where spend exceeded attributed revenue.

### Where did Q disagree or struggle? Why?

The main issues were metric definition and aggregation scope. For Entry 1, Q described the 53.0% figure as a conversion rate, while the matching dashboard visual measures campaign response rate. The numerical value agrees, but the terminology is not equivalent without a defined conversion event. For Entry 4, Q reported $40,722 in won deal revenue for YieldMax Software, while the dashboard's account-level view shows $25,791. This indicates that the two analyses used different aggregation or calculation contexts, so the discrepancy should be validated against the opportunity-level CRM records.

### When would you use Q vs. the dashboard to answer a business question?

Use Q for quick natural-language questions, ad-hoc exploration, and rapid investigation of a specific business issue. Use the dashboard for structured analysis, visual comparison, filtering, recurring KPI monitoring, and management reporting. When Q and the dashboard use different metric definitions or aggregation levels, the dashboard's underlying metric definition should be checked before drawing a business conclusion.
