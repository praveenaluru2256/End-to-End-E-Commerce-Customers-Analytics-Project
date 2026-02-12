# End-to-End-E-Commerce-Customers-Analytics-Project

This project demonstrates a complete modern data engineering solution for analyzing e-commerce customer behavior using a Lakehouse architecture built on Microsoft Fabric.

The solution ingests raw CSV data into Azure Data Lake Storage Gen2, processes it using Fabric Data Pipelines, transforms data using PySpark notebooks, and implements the Medallion Architecture (Bronze, Silver, Gold) to deliver business-ready insights through semantic models and dashboards.

This project simulates a real-world enterprise data platform used for customer analytics and business intelligence.

* Business Objective

  The goal of this project is to:

  Analyze customer purchasing behavior

  Track revenue trends

  Monitor payment performance

  Evaluate customer support patterns

  Analyze website activity behavior

  Generate KPIs for business decision-making

* Technologies Used

  Azure Resource Group

  Azure Data Lake Storage Gen2

  Microsoft Fabric

  Data Factory Pipeline

  Lakehouse Architecture

  PySpark

  Delta Tables

  SQL

 Medallion Architecture

* Dataset Description

  The project includes the following datasets:

 1️⃣ Customers

  customer_id

  name

  email

  location

  registration_date

  2️⃣ Orders

  order_id

  customer_id

  order_date

  order_amount

  product_category

3️⃣ Payments

payment_id

order_id

payment_method

payment_status

payment_date

4️⃣ Support

ticket_id

customer_id

issue_type

resolution_status

created_date

5️⃣ Web Activity

session_id

customer_id

page_visited

session_duration

device_type

🔄 Detailed Data Engineering Workflow
Step 1: Azure Infrastructure Setup

Created Resource Group

Created Azure Data Lake Storage Gen2

Enabled Hierarchical Namespace

Created containers and folders

Step 2: Raw Data Ingestion

Uploaded CSV files into ADLS

Designed folder structure by data domain

Ensured secure access using account keys

Step 3: Data Pipeline Implementation
Get Metadata Activity

Retrieves all files from ADLS folder dynamically

Enables dynamic file processing

ForEach Activity

Iterates through each file

Ensures scalable ingestion

Copy Activity

Transfers files from ADLS → Lakehouse Bronze

Converts files into Delta format

🥉 Bronze Layer (Raw Data)

Purpose:

Store raw ingested data

No transformations

Maintain data lineage

Characteristics:

Stored as Delta tables

Full historical data

Append-only structure

🥈 Silver Layer (Data Cleaning & Standardization)

Performed using PySpark Notebook:

Data Cleaning Operations

Removed duplicate records

Handled null values

Standardized date formats

Converted data types

Trimmed text columns

Validated foreign key relationships

Business Validation

Checked orphan orders

Verified payment consistency

Removed corrupted records

🥇 Gold Layer (Business Aggregations)

Created business-ready aggregated tables:

KPIs Generated:

Total Revenue

Monthly Revenue

Revenue by Product Category

Customer Lifetime Value (CLV)

Average Order Value

Payment Success Rate

Support Ticket Volume

Web Session Analysis

Example Aggregations:

Revenue per Customer

Orders per Month

Revenue by Payment Method

Top 10 Customers by Revenue

📊 Data Modeling

Created relationships:

Customers → Orders (1:M)

Orders → Payments (1:1 or 1:M)

Customers → Support (1:M)

Customers → Web Activity (1:M
