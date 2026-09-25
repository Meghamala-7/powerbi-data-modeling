# Power BI Data Modeling – From Messy Data to Star Schema

## Project Overview

This project focuses on transforming a messy multi-table dataset into a structured and analysis-ready data model using Power BI and Power Query.

The original dataset contained 23 source tables with different types of business data, including customers, orders, products, invoices, payments, shipments, campaigns, inventory, and supporting information.

Through data exploration, cleaning, transformation, and modeling, I consolidated the 23 source tables into a structured 14-table model and built a Star Schema in Power BI.

### Project Transformation

**23 Source Tables → Data Cleaning & Transformation → 14 Structured Tables → Star Schema**

## Tools Used

- Power BI
- Power Query
- Data Modeling
- Star Schema

## Data Model

The original dataset contained 23 source tables. After exploring, cleaning, transforming, and restructuring the data, I consolidated them into 14 structured tables.

### Final Model

#### Dimension Tables
- `dim_customers`
- `dim_products`
- `dim_campaign`
- `dim_geo`
- `dim_order_flags`
- `dim_table`

#### Fact Tables
- `fact_sales`
- `fact_sales_target`
- `fact_campaign_spend`
- `fact_inventory`
- `fact_promotion_coverage`
- `fact_order_process`

#### Supporting Tables
- `security`
- `_measures`

### Transformation

**23 Source Tables → Power Query Transformations → 14 Structured Tables → Star Schema**

## Data Transformation Process

The source data contained 23 separate tables with different structures and purposes. Before building the final model, I first explored the available tables and understood what each table and column represented.

### 1. Data Exploration
- Reviewed the structure and purpose of each source table.
- Examined columns, IDs, keys, measures, and descriptive attributes.
- Identified overlapping information and relationships between tables.

### 2. Data Cleaning
- Removed unnecessary columns and duplicate/helper fields.
- Standardized column names and data structures.
- Cleaned and prepared the data using Power Query.

### 3. Table Restructuring
- Created references from existing queries where required.
- Merged related information where appropriate.
- Consolidated related source tables to reduce unnecessary duplication.
- Separated data into fact and dimension structures.

### 4. Data Modeling
- Identified the appropriate fact and dimension tables.
- Created keys and relationships between tables.
- Organized the final model around a Star Schema.
- Validated relationships and important fact values during the transformation.

### Result

**23 Source Tables → 14 Structured Tables**

The resulting model provides a cleaner foundation for analysis and future dashboard development.

## Data Modeling Standards

To keep the model consistent and easier to maintain, I followed common data modeling practices throughout the transformation.

### Naming Conventions

- Used `snake_case` for table and column names.
- Used prefixes such as `dim_` for dimension tables and `fact_` for fact tables.
- Used consistent suffixes such as `_key` and `_id` for identifiers.
- Applied consistent naming across the model.

### Table Organization

The queries were organized into logical groups:

- **Dimensions** – descriptive attributes used for analysis and filtering.
- **Facts** – transactional, measurable, or event-based data.
- **Support** – supporting tables used for security and calculations.

### Validation

During the transformation process:

- Checked important fact values after major transformations.
- Verified that relationships were behaving as expected.
- Checked filters and connections between tables.
- Used measures to monitor important totals and identify unintended changes.

These practices helped maintain consistency and reduce errors while building the final Star Schema.

## Source-to-Model Transformation

The original dataset contained 23 source tables. These tables were analyzed and transformed into a 14-table analytical model.

| Source Data | Final Model |
|---|---|
| CUST_MASTER | dim_customers |
| Address | dim_customers |
| customer_contacts | dim_customers |
| user_details | dim_customers |
| products | dim_products |
| subcategories | dim_products |
| cities | dim_geo |
| regions | dim_geo |
| CAMPAIGN_LOG | dim_campaign |
| ORDERS_2025 + ORDERS_2026 | fact_sales |
| order_line_items | fact_sales |
| INVOICES + payments + shipments | fact_order_process |
| inventory | fact_inventory |
| sales_targets | fact_sales_target |
| campaign_skus | fact_promotion_coverage |
| ORDERS_2025 + ORDERS_2026 | dim_order_flags |
| security | security |
| Date transformation | dim_table |
| DAX measures | _measures |
