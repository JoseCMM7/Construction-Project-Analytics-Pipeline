# Construction Project Analytics Pipeline

## Overview

This project is an end-to-end data analytics pipeline built using real construction project management data.

The goal is to transform raw operational data into actionable insights that help identify projects requiring management attention, including overdue tasks, unresolved actions, workload issues, and operational risks.

The project is currently in development.

---

## Technologies

- Databricks
- PySpark
- SQL
- Delta Lake
- Power BI

---

## Architecture

The project follows a Bronze / Silver / Gold architecture:

Raw CSV Data
->
Bronze Layer
->
Silver Layer
->
Gold Layer
->
Power BI Dashboard

### Bronze Layer

Stores the raw source data with minimal modification.

Current source datasets:

- Construction project tasks
- Construction project forms

### Silver Layer

Cleans and standardizes the raw data.

Planned transformations include:

- Data type correction
- Date standardization
- Null value analysis
- Duplicate analysis
- Status normalization
- Boolean field standardization
- Derived operational fields

### Gold Layer

Creates business-ready datasets and KPIs for reporting and decision-making.

Planned metrics include:

- Total tasks by project
- Open tasks
- Overdue tasks
- Open actions
- Task completion indicators
- Workload indicators
- Project health metrics
- Projects requiring management attention

---

## Project Objective

The main business question is:

> Which construction projects require management attention, and what operational factors are contributing to their risk?

The analysis will focus on identifying patterns related to:

- Overdue work
- Unresolved actions
- Task status
- Project workload
- Issue causes
- Operational risk

---

## Data Pipeline

The planned pipeline is:

1. Ingest raw CSV files into Databricks.
2. Store source data in Bronze tables.
3. Profile and clean the datasets using PySpark.
4. Create Silver tables with standardized and validated data.
5. Use PySpark and SQL to create aggregated Gold tables.
6. Connect the Gold layer to Power BI.
7. Build an interactive project health dashboard.

---

## Current Progress

- [x] Dataset selected
- [x] Databricks workspace configured
- [x] Bronze tables created
- [ ] Data profiling
- [ ] Silver transformation
- [ ] Gold analytical tables
- [ ] SQL analysis
- [ ] Power BI dashboard
- [ ] Final findings and recommendations

---

## Expected Dashboard

The Power BI dashboard will include indicators such as:

- Total Projects
- Total Tasks
- Open Tasks
- Overdue Tasks
- Open Actions
- Project Health
- Workload by Project
- Issues by Cause
- Projects Requiring Immediate Attention

---

## Repository Structure

```text
construction-project-analytics/
│
├── notebooks/
│   ├── 01_data_profiling
│   ├── 02_bronze_to_silver_tasks
│   ├── 03_bronze_to_silver_forms
│   └── 04_silver_to_gold
│
├── sql/
│   └── project_analysis.sql
│
├── powerbi/
│   └── dashboard_screenshots/
│
└── README.md

## Data Source and License

The datasets used in this project come from the
**Construction Project Management Dataset** published on Kaggle.

Source:
[https://www.kaggle.com/datasets/programmer3/construction-project-management-dataset](https://www.kaggle.com/datasets/claytonmiller/construction-and-project-management-example-data)

The original dataset is licensed under:

**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International
(CC BY-NC-SA 4.0)**

The original data is not owned by this repository.

Any cleaned or transformed versions of the original dataset included in this
repository are derived from the source dataset and are shared under the same
CC BY-NC-SA 4.0 terms.

All ETL logic, PySpark transformations, SQL queries, analytical KPIs,
Databricks notebooks, and Power BI visualizations were created for this
portfolio project.
