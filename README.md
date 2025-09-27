
# Olist E-Commerce Data Engineering Project

## Project Overview
This project demonstrates an end-to-end **Data Engineering pipeline** using **Spark and Databricks**, building a **Bronze → Silver → Gold Medallion architecture**. The goal is to ingest, clean, transform, and aggregate e-commerce data to create **analytics-ready tables** for business reporting.

**Tools & Technologies Used:**
- **Databricks Community Edition**
- **PySpark & Spark SQL**
- **Delta Lake**
- **Python**
- **CSV dataset** from [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/olistbr/brazilian-ecommerce)

---

## Project Architecture

**Medallion Architecture:**  
```
Bronze (Raw) ──► Silver (Cleaned & Standardized) ──► Gold (Aggregated / Business-Ready)
```

- **Bronze Layer:** Raw CSV tables loaded into Databricks (customers, orders, products, sellers, payments, reviews, geolocation).  
- **Silver Layer:** Cleaned data with deduplication, proper data types, timestamp conversion, and standardized tables.  
- **Gold Layer:** Aggregated tables for KPIs and analytics readiness.

---

## Datasets / Tables Used
- `customers`  
- `orders`  
- `order_items`  
- `payments`  
- `products`  
- `sellers`  
- `geolocation`  
- `reviews`  
- `product_category_name_translation`  

---

## Gold Layer KPIs
The following **aggregated tables** were created in the Gold layer:

1. **sales_by_month** – Total sales trend over months  
2. **top_products** – Top 10 products by revenue  
3. **orders_by_state** – Total orders per customer state  
4. **avg_delivery_time** – Average delivery duration for orders  
5. **seller_performance** – Revenue per seller  
 

These tables are **ready for dashboards** in Power BI or Databricks SQL.

---

## Project Steps
1. **Bronze Layer**
   - Ingested raw CSV files into Databricks tables.  
   - Kept original data unchanged for traceability.  

2. **Silver Layer**
   - Cleaned and standardized data:
     - Removed duplicates  
     - Corrected data types  
     - Converted timestamps  
     - Standardized column names  

3. **Gold Layer**
   - Created **business-ready tables** by joining, aggregating, and calculating KPIs.  
   - Demonstrated ability to perform Spark transformations, joins, and aggregations.

---

## How to Run
1. Upload CSV datasets into Databricks **FileStore**.  
2. Run notebooks sequentially:
   ```
   01_ingest_bronze → 02_silver → 03_gold
   ```
3. Check results in **Gold tables**: `olist_dataset.gold.*`  
4. Optionally, connect Gold tables to BI tools for dashboards.

---

## Project Highlights
- Built a **full ETL pipeline** using Spark and Databricks.  
- Implemented **Medallion Architecture** (Bronze → Silver → Gold).  
- Performed **data cleaning, transformation, and aggregation**.  
- Created **analytics-ready tables** for business KPIs.  
- Demonstrated **data engineering best practices** suitable for real-world pipelines.

---

  
