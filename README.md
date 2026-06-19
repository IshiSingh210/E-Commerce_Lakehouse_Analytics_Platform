# E-Commerce Lakehouse Analytics Platform

## Overview

This project demonstrates an end-to-end Lakehouse architecture built on Databricks using the Medallion Architecture (Bronze, Silver, Gold).

The solution ingests raw e-commerce transaction and master data, performs data quality validation and cleansing, builds dimensional models, and exposes business-ready datasets for reporting, analytics, and Databricks Genie.

---

## Tech Stack

* Databricks
* PySpark
* Delta Lake
* Unity Catalog
* Databricks SQL
* Databricks Genie
* Power BI
* GitHub

---

## Architecture

> Insert architecture diagram here

---

## Data Model

### Dimension Tables

* `gld_dim_products`
* `gld_dim_customers`
* `gld_dim_date`

### Fact Table

* `gld_fact_order_items`

### BI View

* `fact_transactions_denorm`

---

## Medallion Architecture

### Bronze Layer

Raw ingestion of source CSV files.

#### Tables

* `brz_products`
* `brz_customers`
* `brz_brands`
* `brz_category`
* `brz_calendar`
* `brz_order_items`

#### Metadata Captured

* Source file name
* Ingestion timestamp

---

### Silver Layer

Data quality and cleansing layer.

#### Transformations

* Duplicate removal
* Data type standardization
* Null value handling
* Category and brand code standardization
* Material spelling correction
* Date normalization
* Currency cleansing
* Sales channel normalization

---

### Gold Layer

Business-ready dimensional model optimized for analytics and reporting.

#### Features

* Customer regional enrichment
* Product hierarchy enrichment
* Calendar attribute generation
* Revenue calculations
* Coupon usage indicators
* Currency conversion to INR

---

## Business Metrics

The platform supports the following business metrics:

* Gross Amount
* Discount Amount
* Net Amount
* Net Amount (INR)
* Coupon Usage
* Weekend Indicator
* Sales by Region
* Sales by Brand
* Sales by Category

---

## Databricks Genie

Natural language analytics is enabled through Databricks Genie.

### Example Questions

* What are the top-selling categories?
* What is the revenue by country?
* How do sales perform across channels?
* How effective are coupon campaigns?

---

## Dashboard

<img width="2199" height="992" alt="image" src="https://github.com/user-attachments/assets/7095e524-96ff-48ff-b431-f3995e023948" />

---

## Project Outcomes

* Built a scalable Lakehouse architecture using Databricks and Delta Lake.
* Implemented Medallion Architecture best practices.
* Created analytics-ready dimensional models.
* Enabled self-service business intelligence through Databricks Genie and Power BI.
* Delivered reliable and governed datasets for reporting and decision-making.
