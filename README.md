# Netflix Analytics ELT Pipeline using dbt & Snowflake

An end-to-end modern data engineering project that builds a scalable ELT pipeline for Netflix analytics using AWS S3, Snowflake, dbt, and BI visualization tools.

This project demonstrates how raw streaming datasets can be ingested, transformed, modeled, tested, and visualized using modern data stack technologies and analytics engineering best practices.

---

# Architecture

Raw Data → Amazon S3 → Snowflake → dbt Transformations → Analytics Layer → Power BI / Looker Studio

---

# Tech Stack

- AWS S3
- Snowflake
- dbt (Data Build Tool)
- SQL
- Power BI
- Looker Studio
- Git & GitHub

---

# Project Overview

The project follows a modern ELT workflow:

## Extract
- Raw Netflix datasets are stored in Amazon S3.

## Load
- Data is loaded from S3 into Snowflake raw tables.

## Transform
- dbt is used to:
  - Build modular SQL models
  - Create staging and mart layers
  - Implement testing and validations
  - Generate documentation and lineage
  - Apply snapshots for historical tracking

## Serve
- Final transformed datasets are consumed in BI dashboards for business analytics and reporting.

---

# Key Features

- End-to-end ELT pipeline implementation
- Cloud-native data warehouse architecture
- Modular dbt transformations
- Data quality testing using dbt tests
- Snapshot implementation (SCD Type 2)
- Reusable macros and documentation
- Analytics-ready dimensional models
- Interactive dashboards and reporting

---

# dbt Concepts Implemented

## Models
Built modular SQL-based transformation models.

## Materializations
Implemented:
- View
- Table
- Incremental Models

## Sources
Configured source definitions for raw Snowflake tables.

## Seeds
Used CSV seed files for reference/static datasets.

## Snapshots
Implemented Slowly Changing Dimensions (SCD Type 2).

## Tests
Added:
- unique
- not_null
- accepted_values
- relationship tests

## Macros
Created reusable Jinja-based SQL logic.

## Documentation
Generated dbt docs and DAG lineage visualization.

---

# Folder Structure

```bash
├── analyses/
├── macros/
├── models/
│   ├── staging/
│   ├── intermediate/
│   └── marts/
├── seeds/
├── snapshots/
├── tests/
├── dbt_project.yml
└── README.md
```

---

# Data Pipeline Workflow

1. Upload raw CSV datasets to Amazon S3
2. Load datasets into Snowflake raw schema
3. Create staging models using dbt
4. Transform and clean datasets
5. Build analytics-ready marts
6. Run dbt tests and validations
7. Generate documentation and lineage
8. Connect BI tools for reporting

---

# Sample Analytics Use Cases

- Content popularity analysis
- Genre trend analysis
- Viewer engagement insights
- Ratings distribution analysis
- Regional content trends
- Year-over-year release analysis

---

# Dashboard & Reporting

The transformed datasets are visualized using:
- Power BI
- Looker Studio

Dashboards provide:
- KPI tracking
- Trend analysis
- Interactive filtering
- Business insights

---

# Learning Outcomes

Through this project, I gained hands-on experience in:

- Modern Data Stack architecture
- Analytics Engineering workflows
- dbt transformations and testing
- Snowflake data warehousing
- ELT pipeline implementation
- Cloud-based analytics systems
- Data modeling and optimization

---

# Future Improvements

- CI/CD integration using GitHub Actions
- Orchestration using Airflow
- Real-time streaming ingestion
- Automated data quality monitoring
- Terraform-based infrastructure provisioning

---

# How to Run the Project

## Clone Repository

```bash
git clone <repository-url>
cd netflix-analytics-pipeline
```

## Install dbt

```bash
pip install dbt-snowflake
```

## Configure Snowflake Profile

Update:
```bash
~/.dbt/profiles.yml
```

## Run dbt Models

```bash
dbt run
```

## Run Tests

```bash
dbt test
```

## Generate Documentation

```bash
dbt docs generate
dbt docs serve
```

---

# Project Highlights

- Built using modern analytics engineering principles
- Demonstrates scalable cloud data architecture
- Implements production-grade dbt workflows
- Follows modular and maintainable design patterns

---

# Author

Tarun Kumar Mishra

- LinkedIn: https://www.linkedin.com/in/tarun-mishra-64b9351a8/
- GitHub: https://github.com/tarun2310
