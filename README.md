# End-to-End-E-Commerce-Customers-Analytics-Project

This project demonstrates the complete implementation of an end-to-end data engineering solution for analyzing e-commerce customer data using Azure Data Lake Storage Gen2 and Microsoft Fabric.
The objective was to design a scalable data architecture that ingests raw CSV files, processes them using a Medallion Architecture (Bronze, Silver, Gold), and prepares business-ready datasets for reporting and analytics.

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
