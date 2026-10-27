# Databricks Sales Data Engineering Project

Azure Databricks-based Sales Data Engineering project demonstrating
Bronze, Silver, and Gold data layers with Delta tables and Power BI reporting.

## Architecture

Excel Files
     ↓
Azure Data Lake Storage
     ↓
Azure Databricks
     ↓
Bronze Layer
     ↓
Silver Layer
     ↓
Gold Layer
     ↓
Power BI

## Technologies

- Azure Data Lake Storage (ADLS)
- Azure Databricks
- PySpark
- Delta Lake
- SQL
- Power BI
- Git
- GitHub

## Bronze Layer

The Bronze layer stores data ingested from Excel files into Delta tables.

Main Bronze tables:

- bronze_customers
- bronze_products
- bronze_sales_transactions
- excel_file_control

The ingestion process identifies NEW and UPDATED Excel files and uses
a control table to track processed files.

## Silver Layer

The Silver layer cleans and transforms Bronze data.

Main Silver tables:

- silver_customers
- silver_products
- silver_sales_transactions

Transformations include:

- Data cleansing
- Duplicate handling
- Data type conversion
- Discount normalization
- Historical transaction price handling
- Net amount calculation
- Customer and product validation

## Gold Layer

The Gold layer provides reporting-ready data.

Main Gold tables:

- gold_sales
- gold_customer_sales
- gold_sales_by_category

The Gold layer is used for Power BI reporting and analysis.

## Data Quality

The project includes validation for:

- Duplicate transaction IDs
- Missing customer IDs
- Missing product IDs
- Customer/product referential integrity
- Missing sales prices
- Missing net amounts
- Invalid discount values
- Historical product price changes

## Git and GitHub

Git is used for version control of Databricks notebooks.

Repository workflow:

Databricks
→ Git Folder
→ Commit
→ Push
→ GitHub

## Reporting

Power BI is connected to the Gold layer for reporting and visualization.

## Project Status

- Bronze ingestion: Completed
- Silver transformation: Completed
- Gold transformation: Completed
- Data quality validation: Completed
- Git/GitHub integration: Completed
- Power BI reporting: Completed
