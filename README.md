# Global Retail Data Engineering Project

This project demonstrates the process of creating a data pipeline for a global retail dataset using **Apache Spark** and **Databricks Community Edition**. The project covers **ETL (Extract, Transform, Load)** processes from raw data to business-level insights.

## Project Overview

The Global Retail project involves processing data for customers, transactions, and products to generate business insights such as daily sales, category sales, and customer behavior. This project is designed as an end-to-end data engineering pipeline using **Apache Spark** for distributed data processing.

### Project Components

1. **Bronze Layer**: Raw, unprocessed data.
   - `bronze_customer`: Contains raw customer information.
   - `bronze_transaction`: Contains transaction records.
   - `bronze_products`: Contains product details.

2. **Silver Layer**: Cleaned and transformed data.
   - `silver_customer`: Contains cleaned customer data.
   - `silver_transaction`: Contains cleaned transaction data.
   - `silver_products`: Contains cleaned product data.

3. **Gold Layer**: Aggregated and business-level insights.
   - `gold_category_sales`: Contains category-wise aggregated sales data.
   - `gold_daily_sales`: Contains daily aggregated sales data.

## Technologies Used

- **Apache Spark**: For distributed data processing.
- **Databricks Community Edition**: For managing and running the Spark environment.
- **SQL**: For querying and transforming data.
- **Python**: For scripting and automation of the ETL processes.

## Setup Instructions

Set up Databricks Environment:
- Create a Databricks Community Edition account if you don't have one.
- Create a new cluster in Databricks.

Load the Data:
- Upload the raw dataset files to Databricks (these could be CSV, JSON, or Parquet files).
- Create a table in the globalretail_bronze database for each of the raw datasets (bronze_customer, bronze_transaction, bronze_products).

Execute the ETL Pipeline:
- Use the Databricks notebooks to run the ETL process and load data from the bronze to silver layer, followed by the aggregation of data into the gold layer.

Query the Results:
- Use SQL or Python to query the final aggregated data stored in the gold layer (e.g., gold_category_sales, gold_daily_sales) to generate business insights.

##Project Structure
globalretail/
├── bronze/
│   ├── bronze_customer
│   ├── bronze_transaction
│   └── bronze_products
├── silver/
│   ├── silver_customer
│   ├── silver_transaction
│   └── silver_products
└── gold/
    ├── gold_category_sales
    └── gold_daily_sales
