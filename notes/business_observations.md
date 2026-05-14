\## 1. Dataset Understanding



\### orders dataset:



\- 99,442 rows, 8 columns

\- order\_delivered\_carrier\_date and order\_delivered\_customer\_date have missing values

\- Missing delivery dates indicate undelivered orders (cancelled/in transit)

\- This is meaningful missing data, not a data quality issue



\### order\_items dataset:



\- 112,651 rows, 7 columns

\- More rows than orders → multiple items per order

\- order\_item\_id represents item sequence within an order

\- Important for calculating correct revenue per order



\### customers dataset:



\- Contains unique customer identifiers and location data

\- Each order is linked to a customer via customer\_id

\- Useful for customer-level and geographic analysis



\### products dataset:



\- Contains product category information

\- Used to analyze category-wise performance

\- Some missing or inconsistent category values handled during loading



\### sellers dataset:



\- Contains seller information and locations

\- Helps analyze seller distribution and performance



\### order\_payments dataset:



\- Contains payment type and payment value

\- Used to analyze revenue contribution and payment behavior

\- Multiple payment records possible per order



\### order\_reviews dataset:



\- Contains review scores and timestamps

\- Useful for analyzing customer satisfaction

\- Some missing review comments observed



\### geolocation dataset:



\- Contains zip code, city, and state mapping

\- Used to derive geographic insights

\- Helps in city-level revenue analysis



2\. DATA CLEANING OBSERVATIONS:



\- Converted date columns using STR\_TO\_DATE()

\- Handled missing values using NULLIF()

\- Ensured correct datetime format for analysis

\- Identified meaningful missing values (not errors)



3\. DATA VALIDATION:



\- Checked for orders without customers → 0 invalid

\- Checked for order\_items without orders → 0 invalid

\- Checked for payments without orders → 0 invalid

\- Checked for reviews without orders → 0 invalid



\- Data integrity maintained across all tables.



4\. BUSINESS ANALYSIS NOTES:



\- Revenue shows seasonal trends with gradual growth

\- Credit card is dominant payment method

\- Some delivery delays observed → logistics improvement needed

\- Orders may contain multiple items → impacts revenue calculation



5\. Advanced Business Insights

\## 5.1 Delivery Performance Analysis



\### Objective

Analyze delayed delivery behavior across sellers, states, and weekdays.



\### Key Findings

\- Certain states showed significantly higher delayed delivery percentages.

\- Monday and Tuesday recorded relatively higher delivery delays.

\- Some sellers consistently underperformed in delivery timelines.



\### Business Impact

Frequent delivery delays negatively affect customer trust and repeat purchase behavior.



\### Recommendation

Implement stricter logistics monitoring for high-delay regions and low-performing sellers.



\### 5.2 Payment Analysis



Objective:

Analyze how payment methods influence order behavior and delivery performance.



Key Findings:

\- Credit cards dominated total transaction volume.

\- Voucher payments showed relatively higher delayed delivery percentages.



Business Impact:

Different payment workflows may affect fulfillment efficiency and operational timelines.



Recommendation:

Optimize non-standard payment verification and settlement workflows.



\### 5.3 Product Category Analysis



Objective:

Identify product categories with high delayed deliveries and strong revenue contribution.



Key Findings:

\- Seasonal and fashion-related categories showed higher delivery delays.

\- Home and furniture categories generated significant order volume.



Business Impact:

Inventory planning and warehouse distribution directly affect delivery efficiency.



Recommendation:

Improve demand forecasting and inventory allocation during peak seasonal periods.



\### 5.4 Revenue Trend Analysis



Objective:

Analyze monthly revenue trends and growth behavior.



Key Findings:

\- Revenue showed strong upward growth across multiple months.

\- Certain months contributed disproportionately to annual revenue.



Business Impact:

The business demonstrates seasonal purchasing behavior and revenue concentration periods.



Recommendation:

Use targeted campaigns and seasonal forecasting during low-performing periods.



\### 5.5 Customer RFM Segmentation



Objective:

Segment customers based on recency, frequency, and monetary contribution.



Key Findings:

\- A small customer group contributed disproportionately to total revenue.

\- Many customers showed low repeat purchase behavior.



Business Impact:

Retaining high-value customers can significantly improve long-term profitability.



Recommendation:

Introduce loyalty programs, personalized recommendations, and retention campaigns for high-value customer segments.

