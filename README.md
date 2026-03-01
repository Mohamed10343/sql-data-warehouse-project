# 🏗 Enterprise-Grade Data Warehouse Implementation

### SQL Server \| Medallion Architecture \| Star Schema \| Stored Procedures

------------------------------------------------------------------------

## 📌 Executive Summary

This project demonstrates the end-to-end implementation of a Modern Data
Warehouse using SQL Server following industry best practices.

The solution consolidates sales data from ERP and CRM systems, applies
structured transformations, and delivers a high-performance analytical
model optimized for reporting and business intelligence.

------------------------------------------------------------------------

## 🧱 Architecture Overview

### Medallion Architecture (Bronze → Silver → Gold)

-   🥉 Bronze Layer -- Raw ingestion from CSV files\
-   🥈 Silver Layer -- Data cleansing & standardization\
-   🥇 Gold Layer -- Business-ready Star Schema

<img width="1282" height="789" alt="DWH Architecture" src="https://github.com/user-attachments/assets/c452eb58-b1bd-4752-b1c8-03fb8d58f035" />



------------------------------------------------------------------------

## ⭐ Sales Data Mart -- Star Schema

### Fact Table: `gold.fact_sales`

-   order_number\
-   product_key\
-   customer_key\
-   order_date\
-   ship_date\
-   due_date\
-   quantity\
-   price\
-   sales_amount

**Sales Formula:**\
`sales_amount = quantity * price`

------------------------------------------------------------------------

## Dimension Tables

### `gold.dim_customers`

Customer demographic and identification attributes.

### `gold.dim_products`

Product classification and cost attributes.

> <img width="1450" height="841" alt="data_model" src="https://github.com/user-attachments/assets/f6ab4087-3dcd-476f-aa4d-eac9a0a5c3f7" />


------------------------------------------------------------------------

## 🔄 ETL Strategy

All ETL processes were implemented using:

-   T-SQL\
-   Stored Procedures\
-   Layer-based transformation logic

### ETL Flow

1.  Load CSV files → Bronze\
2.  Transform & Clean → Silver\
3.  Build Analytical Model → Gold

------------------------------------------------------------------------

## 🚀 Performance Optimization

-   Clustered & Nonclustered Indexing on Fact table\
-   Optimized joins using surrogate keys\
-   Pre-calculated measures for analytical performance

------------------------------------------------------------------------

## 📊 Business Validation Queries

The warehouse was validated using:

-   Total Sales by Year\
-   Sales by Category\
-   Top 10 Customers\
-   Monthly Sales Trend\
-   Revenue vs Quantity Analysis

------------------------------------------------------------------------

## 🛠 Tech Stack

-   Microsoft SQL Server\
-   T-SQL\
-   Stored Procedures\
-   CSV Data Sources\
-   Star Schema Modeling\
-   Medallion Architecture

------------------------------------------------------------------------

## 📂 Project Structure

/data\
    /erp\
    /crm

/sql\
    /bronze\
    /silver\
    /gold\
    /procedures\
    /test_queries

/docs\
    DWH_Architecture.png\
    Star_Schema.png

------------------------------------------------------------------------

## 📈 Future Enhancements

-   Add Date Dimension\
-   Implement SCD Type 2\
-   Add incremental loading\
-   Connect to Power BI\
-   Automate scheduling via SQL Agent

------------------------------------------------------------------------

## 👨‍💻 Author

Mohamed Ibrahim\
Data Engineer
------------------------------------------------------------------------


## 🚀 About Me

I am passionate about designing structured databases and transforming raw datasets into meaningful insights.  
Recently completed the Associate Data Engineer in SQL track and currently building real-world SQL Server projects simulating business workflows.

I am actively seeking Data Engineering Internship opportunities.

## 📫 Connect With Me

📧 Email: mohamedibrahim45469@gmail.com  
🔗 LinkedIn: https://www.linkedin.com/in/mohamed-ibrahim-b2aa1a32b  
