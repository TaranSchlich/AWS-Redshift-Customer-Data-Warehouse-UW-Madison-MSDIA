# AWS Redshift Customer Data Warehouse  
Cloud Data Engineering with Amazon Redshift  

**By: Taran Schlichtmann**

**Date: 11/24/2025**

Demonstrates the end‑to‑end process of building a small cloud data warehouse using Amazon Redshift and Amazon S3. Acting as a data engineer for a fictional event‑ticketing company, I created a Redshift cluster, loaded customer data, executed analytical SQL queries, and exported a filtered customer list for business use.

---

## Project Overview

The goal of this assignment was to:

- Upload raw customer data to Amazon S3  
- Configure and launch a Redshift cluster  
- Create database tables using SQL  
- Load pipe‑delimited data using the Redshift COPY command  
- Execute analytical SQL queries to answer business questions  
- Export a filtered customer list as a CSV file  

This workflow mirrors real-world cloud data engineering tasks used in modern analytics pipelines.

---

## AWS Services Utilized

### Amazon S3
- Created an S3 bucket in the Oregon region (`tickets-###`)
- Added a `/load` folder for staging data
- Uploaded the pipe‑delimited customer data file

### Amazon Redshift
- Launched a two‑node RA3 cluster
- Attached the LabRole IAM role for S3 access
- Created the `customers` table using provided SQL
- Loaded data using a COPY command configured for pipe delimiters
- Ran analytical SQL queries to answer business questions

---

## SQL Analysis Results

### 1. Unique Customers  
49,990  
Counted using a `COUNT(DISTINCT customer_id)` query.

### 2. Customers by State  
The state with the highest number of customers was NT, with:  
1,998 customers

### 3. Jazz‑Loving Customers  
Number of customers who like Jazz:  
12,441

### 4. Hidden Hills Customer Export  
A SQL query was written to filter customers by `city = 'Hidden Hills'`.  
The resulting list was exported from Redshift as a CSV file and submitted for review.

---

## Hidden Hills Customer List (CSV Preview)

Ahmed Kennedy  
Allen Oneal  
Angela Le  
Ann Guerra  
Aphrodite Cline  
Arsenio Puckett  
Benjamin Hartman  
Bianca Arnold  
Blossom Zimmerman  
Brady Bond  
... (full list included in CSV)

---

## Tools & Technologies

- Amazon S3  
- Amazon Redshift  
- SQL (DDL, DML, COPY command)  
- IAM Roles  
- Cloud data warehousing concepts  

---

## Skills Demonstrated

- Cloud data warehouse setup  
- Data ingestion using Redshift COPY  
- SQL analytics and aggregation  
- Exporting query results from Redshift  
- AWS resource management (clusters, buckets, permissions)  
- Understanding of ETL/ELT workflows  

---

## Summary

This assignment provided hands‑on experience with cloud data engineering fundamentals using AWS Redshift. By loading, querying, and exporting customer data, I demonstrated the ability to build and operate a small-scale data warehouse suitable for analytics and reporting.
