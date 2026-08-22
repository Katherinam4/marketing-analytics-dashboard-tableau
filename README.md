# Marketing Analytics Dashboard – Tableau

**[View the live interactive dashboard on Tableau Public →](https://public.tableau.com/app/profile/katherina.mashchenko/viz/MarketingCampaignPerformance_17873957523240/CustomerCampaignOverview)**

No download needed — it opens directly in your browser.  
If you’d rather explore it in Tableau Desktop, the full workbook is available at [`tableau/Marketing_Campaign_Performance.twbx`](tableau/Marketing_Campaign_Performance.twbx).

## Project Overview

This project analyses **customer behaviour & campaign response** together with **paid-media (PPC) performance**.  
It includes data cleaning, feature engineering, and an interactive Tableau workbook with **two dashboards**:

1. **Customer Campaign Overview** – customer-level KPIs, campaign acceptance rates, income-based spending patterns, and behavioural segmentation.
2. **Paid Media Performance** – spend, ROAS, CPA, CTR, budget pacing and platform comparison across nearly 1 000 campaigns.

Key business questions the dashboards answer:

- Which campaign performed best?
- How does customer spending and deal dependency change across income levels?
- How can customers be segmented based on recency and spend?
- How efficient is paid media spend (ROAS, CPA, CTR)?
- Which platforms deliver the best return and how is budget pacing across campaigns?

Click an **Income Band** (Customer dashboard) or a **Platform** (Paid Media dashboard) to filter the related views.

## What’s Included

- **Data Cleaning Notebook** (`marketing_data_cleaning.ipynb`)  
  Cleans the raw marketing dataset and engineers features used in the dashboard (Income Band, Total Spend, Deal Dependency Rate, Customer Action Segment, etc.)

- **Cleaned Datasets** (`data/cleaned/`)  
  - `marketing_campaign_cleaned.csv` – customer & campaign response data  
  - `ppc_campaign_performance_cleaned.csv` – paid-media campaign performance data

- **Tableau Workbook** (`tableau/Marketing_Campaign_Performance.twbx`)  
  Interactive workbook containing:

  ### Customer Campaign Overview
  - KPI cards: Total Customers, Avg Customer Spend, Deal Dependency Rate, Campaign Response Rate
  - Response Rate by Campaign
  - Spend & Deal Dependency by Income
  - Customer Action Segments scatter plot (Champions / At Risk / New-Growing / Low Priority – thresholds based on median Recency & Spend)
  - Filter action: click an income band to filter the KPI tiles and the segmentation view

  ### Paid Media Performance
  - KPI cards: Total Spend, Avg CPA, Avg CTR, Blended ROAS
  - Budget Pacing (Under Budget vs On/Over Budget)
  - ROAS by Platform
  - Spend vs Revenue by Month
  - Platform Performance overview

## Key Insights

**Customer Campaigns**
- The **Response** campaign achieved ~15 % acceptance — roughly 2× higher than every prior campaign.
- Average customer spend increases ~22× from Low to Very High income.
- Deal dependency drops sharply as income rises — from ~27 % (Low income) to ~4 % (Very High income).
- Customers split into 4 roughly even action segments (Champions, At Risk, New/Growing, Low Priority).

**Paid Media**
- **$5.79 M** total spend across the tracked campaigns.
- **9.9×** blended ROAS.
- **519 of 974** campaigns are running on or over budget (455 under budget).

## How to Use

1. **[Open the live dashboard](https://public.tableau.com/app/profile/katherina.mashchenko/viz/MarketingCampaignPerformance_17873957523240/CustomerCampaignOverview)** — works in any browser, no download needed.  
   Switch to the **Paid Media Performance** tab at the top of the workbook.
2. On the Customer dashboard, click a point on the **Spend & Deal Dependency by Income** chart to filter the KPI tiles and the Customer Action Segments scatter plot. Click again to clear.
3. On the Paid Media dashboard, use the platform or budget-pacing marks to explore performance by channel.
4. (Optional, for local editing) Download `tableau/Marketing_Campaign_Performance.twbx` and open it in Tableau Desktop or Tableau Public — the `.twbx` format includes the data extracts, so it opens correctly without needing the CSVs separately.

## Tools Used

- Python (Pandas) – Data cleaning & feature engineering
- Tableau – Interactive dashboards & visualisation
