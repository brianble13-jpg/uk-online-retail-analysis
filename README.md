# UK Online Retail Analysis

SQL analysis of 500k+ transaction records from a UK-based online retailer (Dec 2010 – Dec 2011).

## Tools
- PostgreSQL 18
- Tableau Public

## What's in this repo
- `sql/` — all queries including cleaning, deduplication, and 10+ analytical queries
- `README.md` — this file

## Key findings
- UK accounts for ~92% of total revenue (£8.97m of £9.73m)
- 70% of UK customers are repeat buyers, averaging 8 orders each
- November 2011 was the strongest month (+36% MoM); December drop reflects an incomplete month
- Top product: REGENCY CAKESTAND 3 TIER at £134k revenue
- Dec-2010 cohort stabilises at ~35% retention from month 1 onwards

## Queries covered
1. Monthly revenue trend with MoM growth (LAG)
2. Running revenue total (SUM OVER)
3. Top 10 products by revenue (UK, postage excluded)
4. Top 3 products per country (ROW_NUMBER OVER PARTITION BY)
5. Revenue by country with HAVING filter
6. Average order value (AOV) by month
7. Repeat vs one-time customer split (CASE WHEN + CTE)
8. Customer cohort retention by month (3-CTE pattern)
9. Deduplication by ctid
10. Indexes on CustomerID, Country, InvoiceDate, StockCode

## Dashboard
[View interactive Tableau dashboard](https://public.tableau.com/app/profile/willem.bro/viz/OnlineRetail_17799978872890/Dashboard1)
 
