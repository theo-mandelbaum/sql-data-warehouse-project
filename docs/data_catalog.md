# Data Dictionary for Gold Layer

## Overview

The Gold Layer is the business-level data representation, structured to support analytical and reporting use cases. It consists of dimensino tables and fact tables for specific business metrics

1. gold.dim_customers

- Purpose: The purpose of this dimension is to include all customer details, including demographic and geographic data.

- Columns:

| Column name     | Data Type   | Description |
|-----------------|-------------|-------------|
| customer_key    | INT         | Surrogate key that uniquely identifies each customer record in the dimension table   |
| customer_id     | INT         | Unique identifier for each customer listed |
| customer_number | VARCHAR(50) | Alphanumeric value to represent the customer, used for referencing and tracking |
| first_name      | VARCHAR(50) | First name of the customer |
| last_name       | VARCHAR(50) | Last name of the customer |
| country         | VARCHAR(50) | Country of residence for the customer (e.g., 'United States') |
| marital_status  | VARCHAR(50) | Marital status of the customer (e.g., 'Married') |
| gender          | VARCHAR(50) | Gender of the customer (e.g., 'Male', 'Female') |
| birthdate       | DATE        | Date of birth of the customer formatted YYYY-MM-DD (e.g., 2001-08-03) |
| create_date     | DATE        | Date and time that the customers record was created |
