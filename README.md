# SQL Data Analytics & Exploratory Data Analysis (EDA) Project

## Overview
This repository contains a comprehensive suite of SQL scripts designed to perform deep data exploration, advanced analytics, and automated reporting. Built around a retail/sales data model, this project demonstrates the end-to-end analytical workflow—from initial database setup and data validation to complex time-series trends, customer segmentation, and performance ranking. 

The scripts serve as a robust portfolio of SQL best practices, utilizing a standard star schema to extract actionable business insights regarding product performance and customer behavior.

## Dataset Architecture
The data model utilizes a dimensional modeling approach (Star Schema) consisting of three core files:
* **`fact_sales.csv`**: Contains the core transactional data and metrics.
* **`dim_customers.csv`**: Contains customer attributes and demographic dimensions.
* **`dim_products.csv`**: Contains product details, categories, and hierarchical data.

## Analytical Workflow & Script Structure
The repository is modularly organized into specific analytical themes. Each script focuses on a distinct phase of the data analysis lifecycle:

### 1. Database Setup & Initialization
* **`init_database.sql`**: DDL statements to create the schema, define primary/foreign key relationships, and load the raw CSV data into the relational database.

### 2. Exploratory Data Analysis (EDA)
These scripts validate data integrity, uncover distributions, and establish the analytical baseline:
* **`db_exploration.sql`**: High-level overview of table structures, row counts, and missing values.
* **`dimensions_exploration.sql`**: Profiling categorical data (customers, products) to understand distinct values and groupings.
* **`measures_exploration.sql`**: Analyzing numerical distributions, averages, and statistical outliers in sales data.
* **`date_range_exploration.sql`**: Establishing the temporal boundaries and seasonality of the dataset.

### 3. Advanced Business Analytics
These scripts leverage advanced SQL techniques (Window Functions, CTEs, Complex Joins) to answer specific business questions:
* **`magnitude_analysis.sql`**: Evaluating the sheer scale of metrics (e.g., total revenue by category).
* **`ranking_analysis.sql`**: Identifying top and bottom performers (Top N products, VIP customers) using `RANK()` and `DENSE_RANK()`.
* **`change_over_time.sql`**: Calculating period-over-period growth (MoM, YoY).
* **`cumulative_analysis.sql`**: Calculating running totals and moving averages to smooth out volatility.
* **`part_to_whole_analysis.sql`**: Determining percentage contributions (e.g., % of total revenue driven by a specific region).
* **`performance_analysis.sql`**: Comparing actuals against targets or historical benchmarks.
* **`data_segmentation.sql`**: Grouping customers into distinct cohorts (e.g., recency, frequency, monetary value - RFM).

### 4. Final Reporting
* **`report_customers.sql`**: A consolidated, automated view summarizing customer lifetime value and engagement.
* **`report_products.sql`**: A comprehensive summary of product profitability, inventory turnover, and category performance.

## Core SQL Techniques Demonstrated
* **Data Definition Language (DDL):** Schema creation and data import.
* **Aggregations & Grouping:** `SUM`, `AVG`, `COUNT`, `GROUP BY`, `HAVING`.
* **Window Functions:** `OVER()`, `PARTITION BY`, `LEAD()`, `LAG()`, `RANK()`.
* **Common Table Expressions (CTEs) & Subqueries:** Simplifying complex logic into readable, modular steps.
* **Date & Time Manipulation:** Extracting temporal features for trend analysis.

## How to Run
1. Ensure you have a SQL RDBMS (e.g., PostgreSQL, MySQL, SQL Server) installed.
2. Execute **`init_database.sql`** first to build the schema and populate the tables with the provided `.csv` files.
3. Run the EDA and Analytics scripts sequentially or individually based on the insights you wish to explore.
4. Execute the final reporting scripts (`report_customers.sql`, `report_products.sql`) to generate the final business deliverables.

## License
You are free to use, modify, and share this project with proper attribution.
