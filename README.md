📊 Product Performance Report (SQL)
📌 Project Overview

This project creates a Product Performance Report in SQL Server, consolidating sales and product data.
The report delivers key product-level metrics such as sales, quantity, customer reach, and profitability.
It also classifies products into performance segments (High-Performer, Mid-Range, Low-Performer).

🎯 Objectives

Extract and combine sales and product master data.

Summarize product performance metrics over time.

Segment products based on total sales value.

Compute product KPIs such as recency, revenue trends, and average prices.

🗂️ Key Features

Base Query

Joins sales with product table.

Captures transaction details (date, amount, quantity, customer).

Product Aggregations

Calculates product lifespan (first → last sale).

Measures total orders, total customers, sales, and quantity.

Computes average selling price (ASP) across all orders.

Final Report with KPIs

Performance Segments:

High-Performer → Sales > 50,000

Mid-Range → Sales ≥ 10,000

Low-Performer → Sales < 10,000

KPIs Calculated:

recency_in_months → Months since last sale

avg_order_revenue → Sales ÷ Orders

avg_monthly_revenue → Sales ÷ Lifespan

| Column Name           | Description                                |
| --------------------- | ------------------------------------------ |
| `product_key`         | Unique product identifier                  |
| `product_name`        | Name of the product                        |
| `category`            | Product category                           |
| `subcategory`         | Product subcategory                        |
| `cost`                | Product base cost                          |
| `last_sale_date`      | Last recorded sale                         |
| `recency_in_months`   | Months since last sale                     |
| `product_segment`     | High-Performer / Mid-Range / Low-Performer |
| `lifespan`            | Active sales period (months)               |
| `total_orders`        | Total unique orders                        |
| `total_sales`         | Total sales amount                         |
| `total_quantity`      | Total units sold                           |
| `total_customers`     | Unique customers purchasing this product   |
| `avg_selling_price`   | Average per-unit selling price             |
| `avg_order_revenue`   | Sales ÷ Orders                             |
| `avg_monthly_revenue` | Sales ÷ Lifespan                           |

🛠️ SQL Script

The view is created as:

CREATE VIEW products_Report AS
-- (code provided in repository)


Query results with:

SELECT * FROM products_Report
ORDER BY product_key;

🚀 Use Cases

Product Managers → Identify best and worst performing products.

Sales Teams → Track customer reach and average revenue per product.

Finance Teams → Monitor revenue trends and product contribution.

Business Analysts → Explore pricing and product segmentation patterns.

📂 Repository Structure
📁 Exploratory_Data_Analysis
 ┣ 📄 products_Report.sql   # SQL script for the product report
 ┣ 📄 README.md             # Documentation

✅ Requirements

SQL Server (tested on MS SQL Server)

Database: Exploratory_Data_Analysis

Tables: sales, product

📢 Author

Developed as part of Exploratory Data Analysis (EDA) with SQL to demonstrate product-level performance reporting.
