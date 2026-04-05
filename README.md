# 🎬 MovieLens Data Pipeline (dbt + Snowflake + AWS S3 + Looker Studio)

End-to-end data project building a modern data stack using dbt, Snowflake, AWS S3, and Looker Studio.

---

## 📌 Overview

This project demonstrates how to build a complete analytics pipeline:

- Raw data ingestion from AWS S3
- Data transformation using dbt
- Data warehouse modeling in Snowflake
- Business insights visualization using Looker

---

## 🏗️ Architecture

[S3] → [Snowflake] → [dbt] → [Looker Studio Dashboard]

- **AWS S3**: Stores raw CSV files (MovieLens dataset)
- **Snowflake**: Data warehouse
- **dbt**: Data transformation & modeling
- **Looker**: Dashboard & business insights

---

## 🧱 Data Modeling (dbt)

The project follows a layered approach inspired by modern analytics engineering practices:

project_root/
├── models/
│   ├── staging/                 # Data cleaning & standardization
│   │
│   ├── marts/                   # Final analytical layer (star schema)
│   │   ├── dim/                 # Dimension tables
│   │   ├── fct/                 # Fact tables
│   │
│   └── sources.yml              # Source definitions
│
├── seeds/                       # Static reference data (CSV)
├── tests/                       # Data quality tests
├── macros/                      # Reusable SQL macros
├── snapshots/                   # Slowly changing dimensions (SCD)
├── dbt_project.yml              # Project configuration

---

## 👨‍💻 Author

Luiz Azevedo  
Data & Analytics
