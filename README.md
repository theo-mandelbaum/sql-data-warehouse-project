# Data Warehouse and Analytics Project
This project is my first comprehensive data warehouse! This project involved building a business-ready data warehouse, designed to be used for actionable insights. To acheive this result and follow data engineering best practices, I followed instructions provided in this [video](https://youtu.be/9GVqKuTVANE?si=WBjumq0a1rGCBP-_)

---

## Data Architecture
This warehouse follows the medallion architecture, including **Bronze**, **Silver**, and **Gold** layers. In the "scripts" folder, you can find SQL code for each layer of the architecture.
1. **Bronze Layer**: Stores raw data from the source; in this project, the data appears in the same form as it exists in the provided CSV files.
2. **Silver Layer**: This layer includes the data after it has been cleansed, standardized, and normalized. This layer is meant to prepare data for analysis.
3. **Gold Layer**: Converts business-ready data into a star schema. Afer this layer, data is ready for reporting and analytics.

---

## 🚀 Project Requirements

### Building the Data Warehouse (Data Engineering)

#### Objective
Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

#### Specifications
- **Data Sources**: Import data from two source systems (ERP and CRM) provided as CSV files.
- **Data Quality**: Cleanse and resolve data quality issues prior to analysis.
- **Integration**: Combine both sources into a single, user-friendly data model designed for analytical queries.
- **Scope**: Focus on the latest dataset only; historization of data is not required.
- **Documentation**: Provide clear documentation of the data model to support both business stakeholders and analytics teams.

---

# Notes / Mistakes I Made Thoughout This Process

- Originally, I made the prd_start_dt fields in the bronze.crm_prd_info table DATE fields. However, this was meant to be done during data cleaning, not during table creation.
