# NovaTech Q Exploration Log

**Student Name:** Varad Srivastava  
**Date:** 12 September 2026

## Q Exploration Questions

| # | Question Asked | Q's Answer (summarize) | Dashboard Visual Used to Cross-Check | Dashboard Shows | Match? | Notes |
|---|---|---|---|---|---|---|
| 1 | Which campaign channel has the highest conversion rate? | Direct Mail had the highest conversion rate at 53.0%. | Marketing Funnel — Funnel Stage by Channel | The funnel-stage-by-channel visual provides the channel-level funnel breakdown used to assess conversion. | Yes | Q identified Direct Mail at 53.0%; dashboard funnel provides the corresponding channel-level view. |
| 2 | What is the average deal size by company size? | Enterprise $1,589.17; Small $1,486.49; Medium $1,353.30; Large $1,257.47. | Sales Pipeline — Revenue by Company Size | Enterprise has the highest average deal value, followed by Small, Medium and Large. | Yes | The dashboard ordering and values agree with Q. |
| 3 | What is the average resolution time for critical vs. low-priority tickets? | Critical: 1.79 days; Low: 1.97 days. | Customer Health — Resolution Time by Priority | Critical: 1.79 days; Low: 1.97 days. | Yes | Q and the dashboard agree; low-priority tickets take slightly longer on average than critical tickets. |
| 4 | What are the top 10 accounts by support ticket volume, and what is their total deal revenue? | YieldMax Software ranked highest with 334 support tickets and $40,722 in total won deal revenue. | Customer Health — At-Risk Accounts table | YieldMax Software has 334 support tickets and $25,791 in Won Deal Revenue. | Partial | Q correctly identified YieldMax Software as the highest-ticket-volume account, but its reported deal-revenue figure ($40,722) differs from the dashboard's $25,791. This indicates an aggregation/calculation difference that should be reviewed. |
| 5 | Are there any campaigns where we spent more than we earned back? | Yes. Q identified 6 campaigns where campaign spend exceeded attributed revenue. | Marketing Funnel — Spend vs. Revenue combo chart | The chart shows campaigns where the spend bar is higher than the attributed-revenue line. | Yes | The dashboard confirms the presence of campaigns with spend exceeding attributed revenue. |

## Reflection

### Where did Q agree with the dashboard?

Q agreed with the dashboard on the questions that could be directly supported by the available Topic and dashboard fields. The strongest agreement was for average deal size by company size, resolution time by priority, the highest-support-volume accounts, and campaigns where spend exceeded attributed revenue.

### Where did Q disagree or struggle? Why?

In the initial Topic configuration, Q struggled with campaign-channel conversion and resolution time by priority because the Topic relied on aggregated account-level Marketing and Support data. That aggregation removed ticket-level fields such as `priority` and campaign-level fields such as `campaign_channel`. After the Topic/dashboard configuration was improved and the relevant raw datasets were available, Q was able to answer these questions.

### When would you use Q vs. the dashboard to answer a business question?

Use Q for quick natural-language questions, ad-hoc exploration, and rapid investigation of a specific business issue. Use the dashboard for structured analysis, visual comparison, filtering, recurring KPI monitoring, and management reporting.
