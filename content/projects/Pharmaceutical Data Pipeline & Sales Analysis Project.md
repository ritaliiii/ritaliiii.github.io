+++
title = "Pharmaceutical Data Pipeline & Sales Analysis"
draft = false
showReadingTime = false
showWordCount = false
tags = ["R", "ETL", "SQLite", "MySQL", "Star Schema", "XML", "ggplot2"]
summary = "Built a complete data pipeline and analysis solution for a pharmaceutical sales system."
ShowToc = false

[cover]
  image = "/images/pharma3.jpg"

+++

## Project Overview

This project is a complete data pipeline and analytics solution for a pharmaceutical sales system. It includes:

- **XML data ingestion**
- **Relational and star schema modeling**
- **Partitioned storage for OLTP**
- **Data warehouse design for OLAP**
- **Business analysis using R and `ggplot2`**

---

## Tools

- **Programming Language**: R (for scripting, ETL, analysis, and reporting)
- **Databases**: SQLite (OLTP), MySQL (OLAP with Star Schema)
- **Data Formats**: XML (sales and rep transaction data)
- **Libraries**:
  - Data Handling: `dplyr`, `DBI`, `stringr`
  - XML Parsing: `XML`, `xml2`
  - Visualization & Reporting: `ggplot2`, `kableExtra`, `RMarkdown`
- **Hosting**: FreeMySQLHosting.net (for cloud-based MySQL access)

---

## Highlights

- Successfully parsed and ingested XML data for 4 years of sales transactions.
- Designed and implemented both normalized and dimensional schemas using SQLite and MySQL.
- Automated data partitioning logic and schema transformation in R.
- Produced interactive business analysis reports using RMarkdown, visualized with `ggplot2`.
- Delivered KPIs such as total revenue trends, top-performing reps, and high-selling products.

## Project Structure

- `LoadXML2DB.LiN.R`: Loads XML transaction files into a normalized SQLite database and partitions sales data by year.
- `CreateStarSchema.LiN.R`: Creates and populates a MySQL-based star schema for BI analysis.
- `Sales_Analysis_Report.Rmd`: RMarkdown file using `ggplot2` and `kableExtra` to generate insights from the MySQL star schema.

---

## Database Design

### 1. **Normalized Schema** (SQLite - OLTP)

- Tables: `reps`, `customers`, `products`, `sales`
- Partitioned tables: `sales_2020`, `sales_2021`, `sales_2022`, `sales_2023`

### 2. **Star Schema** (MySQL - OLAP)

- **Dimensions**: `rep_dimension`, `customer_dimension`, `product_dimension`
- **Facts**: `sales_facts`, `rep_facts`

---

## How to Run

### Prerequisites

- R (≥ 4.0)
- Packages: `DBI`, `RMySQL`, `RSQLite`, `XML`, `xml2`, `dplyr`, `ggplot2`, `knitr`, `kableExtra`, `stringr`
- MySQL account (e.g., FreeMySQLHosting.net)

## Visualization Excerpts

<p>
  <img src="/images/pharma1.jpg" width="800" style="float: center;">
</p>

<p>
  <img src="/imagespharma2.jpg" width="1000" style="float: center;">
</p>

[View More Details](https://github.com/ritaliiii/Pharmaceutical-Sales-Data-Pipeline-and-Analysis-Project)
