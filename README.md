# 🛒 Olist Brazilian E-Commerce SQL Analysis

## 📌 Project Overview

This project analyzes the Brazilian E-commerce dataset provided by Olist using advanced SQL techniques. The objective of this project is to uncover business insights related to customer behavior, sales performance, delivery efficiency, payment patterns, and revenue trends.

The project demonstrates real-world data analytics workflow including:

- Data Cleaning
- Data Validation
- Exploratory Data Analysis
- Advanced Business Analysis
- Window Functions
- Revenue Trend Analysis
- Customer RFM Segmentation

This project was built as an end-to-end SQL analytics portfolio project to simulate real business problem-solving scenarios used in the e-commerce industry.


## 🛠️ Tech Stack

- MySQL Workbench
- SQL
- CSV Dataset Files
- Git & GitHub


## 📂 Dataset

The dataset used in this project is the Olist Brazilian E-commerce dataset available on Kaggle.

It contains real-world e-commerce data including:

- Customers
- Orders
- Order Items
- Payments
- Products
- Reviews
- Sellers
- Geolocation Data

Due to dataset size limitations, raw CSV files are not uploaded to this repository.

Dataset download link is provided inside:

raw_data/README.txt



## 📂 Project Structure

```bash
Project1_Olist/
│
├── raw_data/
│   └── README.txt
│
├── sql_scripts/
│   ├── 01_create_database.sql
│   ├── 02_create_tables.sql
│   ├── 03_data_loading.sql
│   ├── 04_data_cleaning_validation.sql
│   ├── 05_business_analysis.sql
│   └── 06_indexes_optimization.sql
│
├── notes/
│   └── business_observations.md
│
├── insights.md
├── README.md
```

## 🔗 Data Source

Dataset: Olist Brazilian E-Commerce Public Dataset

Source:
https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

## ▶️ Project Execution Flow

1. Create database
2. Create tables
3. Load CSV datasets
4. Perform data cleaning
5. Validate data quality
6. Execute business analysis queries
7. Optimize query performance using indexes
8. Generate business insights and observations

## ⚙️ How to Run the Project

1. Download the dataset from the Kaggle link provided.
2. Place all CSV files inside the `raw_data` folder.
3. Open MySQL Workbench.
4. Execute SQL scripts in sequence:

```sql
01_create_database.sql
02_create_tables.sql
03_data_loading.sql
04_data_cleaning_validation.sql
05_business_analysis.sql
06_indexes_optimization.sql
```

5. Review generated business insights and observations.

## 📈 Key Business Problems Solved

- Identified monthly revenue growth trends and seasonal fluctuations
- Analyzed delayed delivery patterns across weekdays and regions
- Evaluated payment behavior and dominant payment methods
- Measured revenue contribution across different months
- Performed month-over-month order growth analysis
- Identified top-performing and low-performing revenue periods
- Analyzed revenue volatility trends over time
- Calculated average revenue per order
- Applied RFM segmentation to identify high-value customers
- Used window functions for ranking, running totals, and growth analysis

## 🌟 Project Highlights

- Built an end-to-end SQL analytics workflow using real-world e-commerce data
- Applied advanced SQL concepts including CTEs and window functions
- Performed revenue, delivery, payment, and customer behavior analysis
- Implemented RFM customer segmentation for business insight generation
- Structured the project using modular SQL execution flow
- Documented business observations and analytical findings professionally
- Prepared the project for future Tableau dashboard integration

## 🚀 Future Improvements

- Build interactive Tableau dashboard
- Add cohort retention analysis
- Perform customer churn analysis
- Build SQL views for dashboard optimization
- Automate reporting workflow





