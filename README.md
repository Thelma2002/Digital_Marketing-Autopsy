# Digital Marketing Autopsy
## Which Campaign Channels Actually Convert? A Data Analysis Pipeline

**Tools:** Python · SQLite · Pandas · Matplotlib · Seaborn
**Dataset:** Marketing Campaign Performance Dataset — Manisha B (Kaggle)
**Sample size:** 20,000 rows (sampled from ~200,000 with random_state=42)
**Notebook:** [https://colab.research.google.com/drive/1S6VoML9ljrn13YqRWStOu9uUr3LF0r5v?usp=sharing]

## The Problem
Marketing managers often allocate budget based on reach (impressions) rather
than actual performance (ROI, conversion rate). This project builds a full
analyst pipeline, from raw data in a SQL database through Python EDA to
surface which channels, campaign types and audience segments actually deliver
results.

## Pipeline
Kaggle CSV → 20k sample → SQLite database → SQL queries → Python EDA → Insights

## Key Findings
1. Influencer campaigns show the highest conversion rate
2. YouTube delivers the best ROI across all channels
3. Health & Wellness and Tech Enthusiast segments convert most efficiently
4. Display have the lowest return on spend, budget reallocation recommended

## SQL Queries
Five business questions answered directly from the SQLite database:
- Conversion rate and ROI by campaign type
- Performance and CTR by channel
- Audience segment analysis
- Top campaign type × channel combinations by ROI
- Performance breakdown by location

## EDA Charts
- Campaign Type: Conversion Rate vs ROI side-by-side comparison
- Channel Performance: 4-metric overview (CVR, ROI, cost, engagement)
- Audience Heatmap: Conversion rate by segment × campaign type
- ROI Distribution: Spread of returns across campaign types

## File Guide
| File | What it does |
|---|---|
| `Marketing_Autopsy.ipynb` | Full pipeline — data loading, SQL, EDA, insights |
| `campaigns_20k_cleaned.csv` | Working dataset with engineered features |
| `SQL_queries/` | SQL query results exported for reference |
| `charts/` | All 4 EDA chart images |

## How I Used AI
Used AI to help structure SQL query syntax, then adapted every query to match
the actual column names and business questions for this specific dataset.
Chart design, analytical interpretation and all recommendations are original.

## Limitations
- Power BI dashboard was scoped out due to time constraints —
  a future version would add an interactive dashboard layer
- Dataset is not time-series so monthly trend analysis is not possible
- ROI and Conversion_Rate are pre-calculated in the source data; a more
  rigorous version would calculate these from raw spend and revenue figures