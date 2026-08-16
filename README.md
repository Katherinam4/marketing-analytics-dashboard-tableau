# Marketing Analytics Dashboard – Tableau

## Project Overview

This project analyzes customer behavior and campaign performance using a marketing dataset.  
It includes data cleaning, feature engineering, and an interactive Tableau dashboard that helps explore key business questions such as:

- Which campaign performed best?
- How does customer spending change across income levels?
- How does deal dependency vary by income?
- How can customers be segmented based on their behavior?

The dashboard allows users to interactively filter by **Income Band** and **Customer Action Segment** to uncover deeper insights.

## What’s Included

- **Data Cleaning Notebook** (`marketing_data_cleaning.ipynb`)  
  Cleans the raw marketing dataset and creates useful features (Income Band, Total Spend, Deal Dependency Rate, Customer Segments, etc.)

- **Cleaned Dataset** (`data/cleaned/`)  
  Ready-to-use data for analysis and visualization

- **Tableau Dashboard** (`tableau/Marketing_Campaign_Performance.twb`)  
  Interactive dashboard with:
  - KPI cards (Total Customers, Avg Customer Spend, Deal Dependency Rate, Campaign Response Rate)
  - Response Rate by Campaign
  - Spend & Deal Dependency by Income
  - Customer Action Segments scatter plot
  - Filter Actions for exploration

## Key Insights

- The **Response** campaign achieved ~15% acceptance — roughly 2× higher than previous campaigns.
- Average customer spend increases significantly from Low to Very High income (approx. 22×).
- Deal dependency drops sharply as income rises (from ~27% to ~4%).

## How to Use

1. Open the Tableau workbook (`tableau/Marketing_Campaign_Performance.twb`) in **Tableau Public** or **Tableau Desktop**.
2. Use the interactive filters:
   - Click on an **Income Band** to filter the view
   - Click on a **Customer Action Segment** to explore different customer groups
3. Clear the selection to return to the full view.

## Tools Used

- Python (Pandas) – Data cleaning & feature engineering
- Tableau – Interactive dashboard & visualization
