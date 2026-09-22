# MonCity Data Warehouse & Business Intelligence

## Overview

This project designs and implements a **data warehouse for MonCity's self-driving car operations** using Oracle SQL. The project integrates booking, maintenance, and accident data to support business intelligence, reporting, and management decision-making.

The project covers the complete data warehousing workflow, including **data exploration, data cleaning, data modelling, star/snowflake schema design, SQL implementation, analytical querying, and Power BI visualisation**.

## Objectives

* Build a data warehouse to support analysis of **bookings, maintenance, and accidents**.
* Improve data quality through data exploration, validation, and cleaning.
* Design a scalable **star/snowflake schema** for business intelligence and reporting.
* Develop SQL queries to analyse fleet utilisation, maintenance performance, and accident patterns.
* Create a Power BI dashboard to communicate insights and support management decisions.

## Technologies

* **Database:** Oracle SQL
* **Data Warehousing:** Star Schema, Snowflake Schema, Fact & Dimension Tables, Bridge Tables
* **Data Processing:** SQL, Data Cleaning, Data Transformation
* **Business Intelligence:** Microsoft Power BI
* **Documentation & Design:** Draw.io / Lucidchart

## Data Warehouse Design

The data warehouse is designed around three main business processes:

1. **Booking**

   * Booking volume
   * Passenger demographics
   * Faculty usage
   * Vehicle utilisation

2. **Maintenance**

   * Maintenance frequency
   * Maintenance costs
   * Maintenance types
   * Research centre involvement

3. **Accidents**

   * Accident frequency
   * Error codes
   * Accident zones
   * Vehicle damage severity

The warehouse uses **fact tables** to store measurable business events and **dimension tables** to provide descriptive attributes for analysis. A bridge table is used where a many-to-many relationship exists between maintenance teams and research centres.

## Data Preparation

Before implementing the data warehouse, the operational database was explored and validated using SQL.

The preparation process included:

* Checking record counts and distinct values.
* Identifying missing and inconsistent data.
* Checking relationships between operational tables.
* Validating categorical values and business rules.
* Cleaning and transforming data before loading it into the warehouse.
* Verifying the cleaned data before analytical processing.

## SQL Implementation

The SQL implementation includes:

```text
sql/
├── 01_Data Exploration & Cleaning.sql
├── 02_Snowflake Schema.sql
└── 03_Data Analysis.sql
```

The analytical queries use SQL techniques including:

* Multi-table joins
* Aggregation
* `GROUP BY`
* Subqueries
* Built-in functions
* Filtering
* Data transformation

## Business Intelligence Dashboard

A **Power BI dashboard** was developed to analyse the warehouse data and identify operational patterns.

The dashboard examines:

* Total bookings
* Maintenance costs
* Maintenance frequency
* Bookings by vehicle type
* Accident frequency
* Accident severity
* Error codes by zone
* Fleet usage by faculty and passenger age group
* Monthly booking trends

## Key Findings

The analysis identified several patterns in the MonCity self-driving fleet:

* The database contained approximately **10,000 booking records**.
* Total maintenance costs were approximately **$303,000**.
* **People Movers** showed a lower maintenance cost per booking compared with Buses and a more favourable accident-severity profile.
* **Error002 (Low Battery)** was the most frequently recorded accident-related error, with **373 accidents**, representing approximately **37% of the 1,000 recorded accidents**.
* Error002 occurred most frequently in **Zone B**, followed by Zone A and Zone C.
* **Information Technology and Engineering** recorded the highest booking volumes.
* February and April showed relatively lower booking demand.

These findings were used to develop recommendations relating to **fleet allocation, battery management, maintenance costs, and booking demand**.

## Repository Structure

```text
moncity-data-warehouse/
│
├── README.md
│
├── dashboard.pdf
│ 
├── snowflake_schema.png
│ 
├── analysis_report.pdf
│
└── sql/
    ├── 01_Data Exploration & Cleaning.sql
    ├── 02_Snowflake Schema.sql
    └── 03_Data Analysis.sql
```

## Key Skills Demonstrated

* Oracle SQL
* Data Warehousing
* Data Modelling
* Star/Snowflake Schema Design
* Fact and Dimension Modelling
* Bridge Tables
* Data Cleaning and Transformation
* SQL Data Analysis
* Business Intelligence
* Power BI
* Data Visualisation
* Data-driven Decision Making

## Note on Data

The original MonCity operational database is **not included in this repository** because the dataset was provided for academic use. SQL scripts and documentation are included to demonstrate the database design, data preparation, warehouse implementation, and analytical approach.

## Project Outcome

This project provided practical experience in designing a data warehouse from an operational database and transforming raw operational data into structured information for **business intelligence, reporting, and management decision-making**.
