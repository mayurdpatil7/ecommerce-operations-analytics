# Olist Brazilian E-Commerce SQL Analysis

End-to-end SQL analytics project analyzing 100,000+ orders across 8 relational 
tables to answer one business question:

**Where is revenue at risk, and what should the business do about it?**

---

## Business Problem

E-commerce platforms grow fast but lose customers silently. This project 
identifies where Olist's revenue is concentrated, where customers are churning, 
what is driving bad reviews, and which operational problems have the highest 
business impact.

---

## Dataset

Source: Kaggle — Olist Brazilian E-Commerce Public Dataset  
100,000+ orders | 8 relational tables | 2016–2018  

Dataset download: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

---

## Key Findings

**67.2% of the customer base is Hibernating or Lost.**
The platform's active engaged customer base is far smaller than raw user 
counts suggest. An At-Risk win-back campaign targeting 18,430 customers 
at day 75 of inactivity is the single highest-ROI retention action 
available, with estimated recoverable revenue of R$ 440,795.

**Delivery delay is the only variable with a direct, measurable impact on 
review scores.**  
On-time orders average 4.29/5.0. Orders delayed 5+ days average 1.70/5.0 — 
a 2.59-point drop driven entirely by operational failure, not product quality. 
Northeast states show 2.1x higher late delivery rates than São Paulo. Lifting 
on-time delivery from 91.9% to 95% is estimated to raise the platform rating 
from 4.16 to 4.36.

**Revenue is dangerously concentrated at the seller level.**  
The top 10% of sellers generate 66.8% of total platform revenue. Losing a 
small number of top sellers creates outsized business risk — a dependency 
that is invisible without seller-level revenue analysis.

**The top revenue category is also the biggest satisfaction liability.**  
beleza_saude is the highest revenue category at R$ 1,446,622 and 9.1% of 
total revenue — but carries a below-average review score. Cross-referencing 
revenue and review data reveals a compound risk not visible in either metric 
alone.

---

## Analytical Approach

Six scripts built in dependency order — database creation, table setup, data 
loading, cleaning and validation, business analysis, and index optimization.

Data quality was validated before any analysis: duplicate checks, null 
handling on critical columns, referential integrity across all 8 tables, 
and order status distribution confirmed.

Business analysis implemented across five dimensions: revenue trends, delivery 
performance, payment behavior, product and category analysis, and regional 
distribution — each producing specific, quantified findings.

RFM segmentation classified 94,983 customers into five behavioral tiers — 
Champions, Loyal, At-Risk, Hibernating, and Lost — with segment-specific 
retention recommendations and estimated revenue impact per action.

Cross-dimensional analysis connected delivery delay directly to review scores, 
revenue concentration to seller dependency risk, and geographic revenue 
distribution to logistics infrastructure gaps — producing findings that no 
single-dimension analysis would reveal.

---

## Key Business Recommendations

Five prioritized actions with estimated impact:

Revenue recovery — trigger At-Risk win-back campaign at day 75 of inactivity, 
estimated R$ 440,795 recoverable revenue across 18,430 customers.

Delivery SLA — enforce 4-day maximum delivery for Tier 1 cities, estimated 
platform rating lift from 4.16 to 4.36.

Seller quality — intervene on high-revenue, low-rating sellers in top 5 
categories, estimated +8 to +12 platform NPS improvement.

Payment optimization — promote installment options for orders above R$ 200, 
where installment buyers spend 105.2% more per order on average.

Geographic expansion — sequence Northeast logistics partnerships before 
marketing expansion, targeting Fortaleza, Recife, and Salvador where purchasing 
intent exceeds current supply.

---

## SQL Concepts Demonstrated

CTEs for multi-step staged calculations, window functions for ranking and 
running totals, RFM scoring using NTILE and composite segmentation logic, 
multi-table JOINs across 8 relational tables, conditional aggregation, 
NULLIF for divide-by-zero protection, index optimization for query performance, 
and data cleaning with duplicate handling and null validation.

---

## Insights

See [insights.md](insights.md) for full findings, regional breakdowns, 
RFM segment tables, and business recommendations with estimated impact figures.

## Dashboard

Interactive Tableau dashboard built on this analysis:  
Live Dashboard - [https://public.tableau.com/app/profile/mayur.patil7608/viz/OlistE-CommercePerformanceCustomerAnalyticsDashboard/Dashboard1]

TABLEAU_GITHUB_URL - [https://github.com/mayurdpatil7/olist-ecommerce-performance-dashboard]

