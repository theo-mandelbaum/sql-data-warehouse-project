# Data Dictionary for Gold Layer

## Overview

The Gold Layer is the business-level data representation, structured to support analytical and reporting use cases. It consists of dimensino tables and fact tables for specific business metrics

1. gold.dim_customers

- Purpose: The purpose of this dimension is to include all customer details, including demographic and geographic data.

- Columns:

| Column Name     | Data Type   | Description |
|-----------------|-------------|-------------|
| customer_key    | INT         | Surrogate key that uniquely identifies each customer record in the dimension table   |
| customer_id     | INT         | Unique identifier for each customer |
| customer_number | VARCHAR(50) | Alphanumeric value to represent the customer, used for referencing and tracking |
| first_name      | VARCHAR(50) | First name of the customer |
| last_name       | VARCHAR(50) | Last name of the customer |
| country         | VARCHAR(50) | Country of residence for the customer (e.g., 'United States') |
| marital_status  | VARCHAR(50) | Marital status of the customer (e.g., 'Married') |
| gender          | VARCHAR(50) | Gender of the customer (e.g., 'Male', 'Female') |
| birthdate       | DATE        | Date of birth of the customer formatted YYYY-MM-DD (e.g., 2001-08-03) |
| create_date     | DATE        | Date that the customer's record was created |


2. gold.dim_products

- Purpose: The purpose of this dimension is to include all product details and their attributes

- Columns:

| Column Name    | Data Type   | Description |
|----------------|-------------|-------------|
| product_key    | INT         | Surrogate key that uniquely identifies each product record |
| product_id     | INT         | Unique identifier for each product |
| product_number | VARCHAR(50) | Alphanumeric value to represent the product, used for referencing and tracking |
| product_name   | VARCHAR(50) | Name of the product (e.g, 'Mountain Bottle Cage') |
| category_id    | INT         | Unique identifier for the category of the product |
| category       | VARCHAR(50) | Name of the broader classification of the product (e.g., 'Accessories') |
| subcategory    | VARCHAR(50) | Name of the more detailed classification of the product, within the category (e.g., 'Cleaners') |
| maintenance    | VARCHAR(50) | Inidicates whether the product requires maintenance or not (e.g., 'Yes', 'No' ) |
| cost           | INT         | The price of each product in dollars |
| product_line   | VARCHAR(50) | The specific series or product line that the product belongs to (e.g., 'Mouintain', 'Touring') |
| start_date     | DATE        | Date that the product became available for sale or use |


3. gold.fact_sales

- Purpose: The purpose of this fact is to include all sales information, as well as relate it to the products and customers data

- Columns:

| Column Name    | Data Type   | Description |
|----------------|-------------|-------------|
| order_number   | VARCHAR(50) | Alphanumeric value to represent each specific order |
| product_key    | INT         | Key representing the prodcut that was involved in an order |
| customer_key   | INT         | key representing the customer who placed an order |
| order_date     | DATE        | Date that the order was placed |
| shipping_date  | DATE        | Date that the order was shipped |
| due_date       | DATE        | Date that the order payment was due |
| sales_amount   | INT         | Total monetary value of the sale |
| quantity       | INT         | Total number of units of the product that were ordered |
| price          | INT         | Price per unit of the product that was ordered |
