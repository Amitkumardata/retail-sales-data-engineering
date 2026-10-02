# An end to end azure data engineer project built with azure data factory, azure data lake storage Gen 2 , azure Databricks and pyspark

## Project Overview

This project Implements a cloud-based retail sales data platform on azure.
It ingest operational retail sales data , store raw data in azure data lake storage Gen 2, applies data quality and transformation rules through azure data bricks and pyspark, and publishes curated dataset for analytics and business reporting 

The platform follows a layered data architecture:
Source system-> landing->bronze->silver->Gold->reporting and Analytics

## Business Problem

Retail sales data arrive from operational source system and may contain incomplete record , inconsistent category values, invalid sales amounts and duplicates transaction. using this data directly for reporting can produce unreliable sales metrics and inconsistent business decisions.

The platform addresses this by automating ingestion, retaining raw source data for traceability ,validating and standardizing records and creating curated analytics datasets


## Business Objectives
Create a reliable and scalable ingestions process for retail sales data
-Retain raw data for auditing ,replay and issues investigation
-Imporve data quality before data is sued by reporting team
- provide trsuted silver and gold dataset for anal



## Repository Structure

```text
1-data-ingestion-adf/
├── ingestion/
│   ├── README.md
│   └── pipeline-notes/
├── medallion-architecture/
│   ├── README.md
│   └── BRONZE_TO_SILVER.md
├── notebooks/
│   └── README.md
├── docs/
│   └── README.md
├── README.md
└── .gitignore
```



