# GCP BigQuery – E-Commerce Sales Analysis

## 📌 Project Overview

This project demonstrates how **Google Cloud Platform (GCP) BigQuery** can be used to analyze e-commerce sales data using SQL.

An e-commerce company receives approximately 1,000 orders daily. The business team wants to identify high-revenue sales, top-performing products, valuable customers, inactive customers, and monthly sales trends.

This project uses BigQuery SQL queries to clean order data, calculate revenue, analyze customer purchasing behavior, and generate sales reports.

## 🎯 Project Objectives

- Remove duplicate orders from the dataset.
- Calculate net revenue from completed orders.
- Identify the top three products in each region.
- Find inactive customers based on their last purchase date.
- Identify customers who purchase continuously for three or more months.
- Generate a Customer Lifetime Value (CLV) report.
- Analyze monthly sales performance.
- Find products with unit prices below ₹10,000 in a specific month.
- Identify customers who repeatedly purchase a particular product.
- Generate monthly sales reports for individual products.

## 🛠️ Technologies Used

- **Google Cloud Platform (GCP)**
- **Google BigQuery**
- **SQL**
- **Common Table Expressions (CTEs)**
- **Window Functions**
- **Aggregate Functions**
- **Date and Time Functions**

## 📊 Dataset Description

The project uses an e-commerce orders dataset containing the following fields:

| Column Name | Description |
|---|---|
| `order_id` | Unique identifier for an order |
| `customer_id` | Identifier for a customer |
| `order_date` | Date on which the order was placed |
| `product_id` | Identifier for a product |
| `product` | Name of the product |
| `quantity` | Quantity of products ordered |
| `unit_price` | Price per product unit |
| `region` | Region associated with the order |
| `status` | Current order status |

The dataset includes products such as laptops, mobile phones, headphones, keyboards, and monitors.

## ✅ Tasks Performed

### Task 1: Remove Duplicate Orders
Identified duplicate orders using SQL window functions and created a cleaned table to support further analysis.

**SQL concepts:** `ROW_NUMBER()`, `PARTITION BY`, `CREATE TEMP TABLE`.

### Task 2: Calculate Net Revenue
Calculated revenue from completed orders using the quantity and unit price.

**Formula:**

Net Revenue = Quantity × Unit Price

**SQL concepts:** `SUM()`, `WHERE`, aggregate functions.

### Task 3: Find the Top 3 Products in Each Region
Ranked products by total revenue within each region to identify the best-performing products.

**SQL concepts:** `SUM()`, `RANK()`, `PARTITION BY`, `ORDER BY`.

### Task 4: Identify Inactive Customers
Analyzed customers' latest purchase dates to identify customers who have not purchased recently.

**SQL concepts:** `MAX()`, `GROUP BY`, `DATE_DIFF()`.

*Note: An inactivity threshold should be defined when applying this analysis to real business data.*

### Task 5: Find Customers Purchasing Continuously for 3 Months
Analyzed monthly purchase activity to identify customers with purchases across consecutive months.

**SQL concepts:** `DATE_TRUNC()`, `LAG()`, window functions, `COUNT()`.

### Task 6: Build a Customer Lifetime Value Report
Calculated customer-level metrics to understand purchasing behavior and lifetime revenue.

The report includes:
- Total orders
- Total quantity purchased
- Lifetime revenue
- Average order value
- First purchase date
- Last purchase date

**SQL concepts:** `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`.

### Task 7: Find Monthly Sales
Aggregated completed orders by month to analyze sales trends.

The report includes:
- Total orders
- Total quantity sold
- Monthly revenue

**SQL concepts:** `FORMAT_DATE()`, `COUNT()`, `SUM()`, `GROUP BY`.

### Task 8: Find Products with Unit Prices Below ₹10,000
Filtered orders to identify products with unit prices below 10,000 during a selected month.

**SQL concepts:** `WHERE`, date filters, comparison operators.

### Task 9: Identify Repeat Customers for a Particular Product
Identified customers who purchased a selected product multiple times during a six-month period.

**SQL concepts:** `COUNT(DISTINCT order_id)`, `GROUP BY`, `HAVING`.

### Task 10: Generate Monthly Sales Reports for Each Product
Created product-level sales summaries for a selected month.

The report includes:
- Product ID
- Product name
- Total quantity sold
- Total orders
- Total sales revenue

**SQL concepts:** `SUM()`, `COUNT()`, `GROUP BY`, `ORDER BY`.

## ☁️ Platform and Implementation

The project was implemented using Google BigQuery.

General workflow:

1. Open the Google Cloud Console.
2. Select the appropriate GCP project.
3. Open BigQuery in the Google Cloud Console.
4. Create or select a dataset.
5. Create the orders table and load or insert the sample data.
6. Execute SQL queries to clean and analyze the data.
7. Review query results and generate reports.

## 📈 Expected Outcomes

This project demonstrates how SQL-based analytics can help businesses:

- Improve data quality by removing duplicate orders.
- Understand revenue generation.
- Identify top-performing products and regions.
- Understand customer purchasing patterns.
- Measure customer lifetime value.
- Monitor monthly sales performance.
- Support data-driven business decisions.

## 🚀 Skills Demonstrated

- Writing SQL queries in BigQuery.
- Cleaning and transforming structured data.
- Using window functions for ranking and deduplication.
- Performing revenue and sales calculations.
- Analyzing customer behavior.
- Generating business reports.
- Working with Google Cloud Platform.

## 👨‍💻 Author

**Name:** M. Sainath Reddy

**USN:** 23BTRCL213

**HCL ID:** HCLTFP2265832

## 📝 Conclusion

The GCP BigQuery E-Commerce Sales Analysis project demonstrates how cloud-based data analytics can transform raw order records into meaningful business insights.

By applying SQL queries in BigQuery, the project supports data cleaning, revenue analysis, product ranking, customer segmentation, and monthly sales reporting.
