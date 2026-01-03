# Data Dictionary for Gold Layer

## Overview

The Gold Layer is the business-level data representation, structured to support analytical and reporting use cases. It consists of dimensino tables and fact tables for specific business metrics

1. gold.dim_customers

- Purpose: The purpose of this dimension is to include all customer details, including demographic and geographic data.

- Columns:

| Column name   | Data Type | Description |
|---------------|-----------|-------------|
| customer_key  | INT       | Surrogate key that uniquely identifies each customer record in the dimension table |
| customer_id   | INT       | Unique identifier for each customer listed |
