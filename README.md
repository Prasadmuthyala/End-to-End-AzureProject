# End-to-End Azure Data Engineering Project

## Overview

This project demonstrates an **end-to-end data engineering pipeline** implemented using **Azure Databricks**, **Azure Data Factory (ADF)**, **Azure Logic Apps**, **SQL Databases**, and various data sources such as **CSV**, **XLSX**, **JSON**, **PostgreSQL**, **SQL databases**, and **APIs**. The pipeline follows the **Medallion Architecture** and is designed to ingest, transform, and process large-scale data, storing it in a structured, clean format ready for reporting and analysis.

The project also includes integration with **Azure Logic Apps** for email notifications, ensuring that stakeholders are informed of pipeline successes or failures.

---

## Table of Contents

- [Project Description](#project-description)
- [Technologies Used](#technologies-used)
- [Data Pipeline Architecture](#data-pipeline-architecture)



---

## Project Description

This repository contains an **end-to-end data pipeline** that extracts data from multiple sources, transforms it, and loads it into an analytics-ready data store using **Medallion Architecture**.

Key steps of the project involve:
- **Ingestion**: Pulling data from multiple sources like **CSV**, **XLSX**, **JSON**, **PostgreSQL**, **SQL databases**, and **APIs**.
- **Transformation**: Data is processed, cleaned, and transformed using **Azure Databricks** (Apache Spark).
- **Storage**: Cleaned and transformed data is stored in **Azure SQL Database**.
- **Aggregation**: Aggregated views are created for reporting and analytics in the **Gold Layer**.

The solution also leverages **Azure Logic Apps** to send **email notifications** on key pipeline events, ensuring transparency and real-time alerts for data engineers or stakeholders.

---

## Technologies Used

- **Azure Databricks**: For scalable data processing, transformation, and analysis with Apache Spark.
- **Azure Data Factory (ADF)**: For orchestrating ETL processes, moving data between systems.
- **Azure Logic Apps**: For sending email notifications upon pipeline completion, success, or failure.
- **Azure SQL Database**: For storing processed and structured data.

**Data Sources**:
- **CSV**: Data files in Comma Separated Values format.
- **XLSX**: Data in Microsoft Excel format.
- **JSON**: Data in JavaScript Object Notation format.
- **PostgreSQL**: Data sourced from PostgreSQL databases.
- **SQL databases**: Data from structured SQL-based databases.
- **APIs**: External data sources accessed via API requests.

---

## Data Pipeline Architecture

The project follows the **Medallion Architecture**, a multi-layer data architecture that allows for scalable and structured data processing.

1. **Bronze Layer (Raw Data)**: 
   - Raw data from sources like CSV, XLSX, JSON, and APIs is ingested and stored.
   - The data is loaded into **Azure Data Lake Storage** or a similar raw storage solution.

2. **Silver Layer (Cleaned Data)**:
   - The raw data is processed and cleaned using **Azure Databricks**.
   - Data is validated, transformed, and enriched before being loaded into the **Azure SQL Database**.

3. **Gold Layer (Aggregated Data)**:
   - The data is aggregated and transformed into analytics-ready forms.
   - Aggregated tables and views are created and stored in **Azure SQL Database** for reporting and analysis.

Additionally, **Azure Logic Apps** are integrated to send **email notifications** (such as success or failure emails) whenever specific events occur in the pipeline, like completion or errors.

---


