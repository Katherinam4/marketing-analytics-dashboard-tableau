# Marketing Analytics Dashboard – Tableau

**[View the live interactive dashboard on Tableau Public →](https://public.tableau.com/views/Marketing_Campaign_Performance_17868902953440/MarketingOverview?:language=en-GB&:display_count=n&:origin=viz_share_link)**

No download needed — it opens directly in your browser. If you'd rather explore it in Tableau Desktop, the full workbook is available at [`tableau/Marketing_Campaign_Performance.twbx`](tableau/Marketing_Campaign_Performance.twbx).

## Project Overview

This project analyzes customer behavior and campaign performance using a marketing dataset. It includes data cleaning, feature engineering, and an interactive Tableau dashboard that helps explore key business questions such as:

- Which campaign performed best?
- How does customer spending change across income levels?
- How does deal dependency vary by income?
- How can customers be segmented based on their behavior?

The dashboard lets you click an income band to filter the KPI tiles and customer segmentation view down to that specific group.

## What's Included

- **Data Cleaning Notebook** (`marketing_data_cleaning.ipynb`)
  Cleans the raw marketing dataset and engineers features used in the dashboard (Income Band, Total Spend, Deal Dependency Rate, Customer Action Segment, etc.)
- **Cleaned Dataset** (`data/cleaned/`)
  Ready-to-use data for analysis and visualization
- **Tableau Workbook** (`tableau/Marketing_Campaign_Performance.twbx`)
  Interactive dashboard with:
  - KPI cards (Total Customers, Avg Customer Spend, Deal Dependency Rate, Campaign Response Rate)
  - Response Rate by Campaign
  - Spend & Deal Dependency by Income
  - Customer Action Segments scatter plot (calculated field, quadrant thresholds based on median Recency/Spend)
  - Filter action: click an income band to filter the rest of the dashboard

## Key Insights

- The **Response** campaign achieved ~15% acceptance — roughly 2x higher than every prior campaign.
- Average customer spend increases ~22x from Low to Very High income.
- Deal dependency drops sharply as income rises — from ~27% (Low income) to ~4% (Very High income).
- Customers split into 4 roughly even action segments (Champions, At Risk, New/Growing, Low Priority), with 565 customers flagged specifically as high-value but going quiet ("At Risk").

## How to Use

1. **[Open the live dashboard](https://public.tableau.com/views/Marketing_Campaign_Performance_17868902953440/MarketingOverview?:language=en-GB&:display_count=n&:origin=viz_share_link)** — works in any browser, no download needed.
2. Click a point on the **Spend & Deal Dependency by Income** chart to filter the KPI tiles and the Customer Action Segments scatter plot down to that income band. Click it again to clear.
3. (Optional, for local editing) Download `tableau/Marketing_Campaign_Performance.twbx` and open it in Tableau Desktop or Tableau Public — the `.twbx` format includes the data, so it opens correctly without needing the CSVs separately.

## Tools Used

- Python (Pandas) – Data cleaning & feature engineering
- Tableau – Interactive dashboard & visualization
