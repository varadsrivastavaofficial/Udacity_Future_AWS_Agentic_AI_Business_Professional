# SPICE Import Evidence Log

## NovaTech Revenue Intelligence Dashboard

### Purpose

This log documents successful SPICE ingestion of the three original
source datasets used for the NovaTech Revenue Intelligence Dashboard.
The displayed column counts include calculated fields added during
preparation; the original source datasets each contained 20 columns.

### 1. CRM Dataset

-   **Source file:** `novatech_crm_deals.csv`
-   **SPICE ingestion status:** Completed
-   **Rows imported:** 499
-   **Original source columns:** 20
-   **Calculated columns added:** 2
-   **Displayed dataset columns:** 22
-   **Calculated columns:** `Won Deal Revenue`, `High Value Deal Flag`
-   **Evidence screenshot:** `CRM_SPICE_499_rows_20_source_columns.png`

### 2. Marketing Dataset

-   **Source file:** `novatech_marketing_campaigns.csv`
-   **SPICE ingestion status:** Completed
-   **Rows imported:** 2,240
-   **Original source columns:** 20
-   **Calculated columns added:** 3
-   **Displayed dataset columns:** 23
-   **Calculated columns:** `Campaign ROI`, `Total Product Spend`,
    `Lead Engagement Score`
-   **Evidence screenshot:**
    `Marketing_SPICE_2240_rows_20_source_columns.png`

### 3. Support Dataset

-   **Source file:** `novatech_support_tickets.csv`
-   **SPICE ingestion status:** Completed
-   **Rows imported:** 3,000
-   **Original source columns:** 20
-   **Calculated columns added:** 2
-   **Displayed dataset columns:** 22
-   **Calculated columns:** `Resolution Time (days)`, `Is Resolved`
-   **Evidence screenshot:**
    `Support_SPICE_3000_rows_20_source_columns.png`

### Evidence Interpretation

The QuickSight dataset summary screens show successful SPICE ingestion
and the imported row counts. The displayed column count is higher than
the original 20-column source structure because calculated fields were
added during dataset preparation.

### Verification

  ---------------------------------------------------------------------------
  Source              Rows     Original        Added    Displayed SPICE
  Dataset         Imported      Columns   Calculated      Columns Status
                                             Columns              
  ----------- ------------ ------------ ------------ ------------ -----------
  CRM                  499           20            2           22 Completed

  Marketing          2,240           20            3           23 Completed

  Support            3,000           20            2           22 Completed
  ---------------------------------------------------------------------------
