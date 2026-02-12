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

🧰 Technologies Used

Azure Resource Group

Azure Data Lake Storage Gen2

Microsoft Fabric

Data Factory Pipeline

Lakehouse Architecture

PySpark

Delta Tables

SQL

Medallion Architecture

📂 Project Workflow
1️⃣ Azure Setup

Created Resource Group

Created ADLS Gen2 with Hierarchical Namespace

Created containers and folder structure

Uploaded raw CSV files

2️⃣ Data Migration Pipeline

Used Get Metadata activity to retrieve file list

Implemented ForEach activity to iterate dynamically

Used Copy Activity to move files into Bronze layer

Validated pipeline execution
