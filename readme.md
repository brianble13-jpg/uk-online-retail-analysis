# UK Online Retail Analysis

SQL analysis of 500k+ e-commerce transactions using PostgreSQL.

## Project Overview

End-to-end analysis of the UCI Online Retail dataset (~540k transactions, Dec 2010 – Dec 2011). 
Data was loaded into PostgreSQL, cleaned, and analysed using window functions, CTEs, and aggregati

sql/
├── schema.sql          -- table definition
├── load.sql            -- COPY command to load CSV into PostgreSQL
├── cleaning.sql        -- deduplication, null removal, bad data filtering
└── queries/
└── revenue_analysis.sql  -- 10 analytical queries

## Queries

1. Monthly revenue trend with month-on-month growth (LAG)
2. Running revenue total (SUM OVER)
3. Top 10 products by revenue (UK, excluding postage)
4. Top 3 products per country (ROW_NUMBER OVER PARTITION BY)
5. Revenue by country (all countries, returns excluded)
6. Average order value by month
7. Repeat vs one-time customer split
8. Customer cohort retention by month
9. Standard aggregations — revenue by country with HAVING filter
10. Indexes on CustomerID, Country, InvoiceDate, StockCode

## Key Findings

- 536k rows after deduplication (5,429 duplicate rows removed)
- UK accounts for ~92% of total revenue (£8.97m of £9.73m)
- 70% of UK customers are repeat buyers, averaging 8 orders each
- Peak month: November 2011 (+36% MoM); December 2011 incomplete
- Dec 2010 cohort retention stabilises at ~35% after month 1

## Tools

PostgreSQL · pgAdmin · VS Code