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

## Final Data Model

![Final Star Schema](Screenshots/final-star-schema.png)
