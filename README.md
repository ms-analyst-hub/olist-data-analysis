# Olist E-commerce Analytics

**End-to-end Data Analyst portfolio project | Python • MySQL • Power BI**

This project analyzes the Brazilian E-Commerce Public Dataset by Olist using a structured analyst workflow: **data preparation → relational modeling → SQL validation → business-rule checks → dashboard reporting**.

The focus is not simply on producing charts. The project demonstrates how an analyst validates data quality and business logic before trusting KPIs and reporting results.

## Business Questions

- How are orders and revenue trending over time?
- Which product categories and sellers contribute most to sales?
- How does delivery performance vary across orders?
- Which payment methods and installment patterns are most common?
- How do review scores relate to customer experience?
- Are the underlying tables reliable enough for KPI reporting?

## Analytics Workflow

1. **Data preparation — Python / Pandas**
   - Standardize columns and data types
   - Parse dates and numeric fields
   - Preserve legitimate business nulls
   - Remove exact duplicate rows where appropriate
   - Prepare analysis-ready files

2. **Relational modeling — MySQL**
   - Model the Olist tables using primary keys and composite keys
   - Define table grain and relationships
   - Prepare SQL loading scripts

3. **Data quality & business validation — SQL**
   - Row-count reconciliation
   - Duplicate and null checks
   - Date/timeline sanity checks
   - Review-score validation
   - Payment and price sanity checks
   - Order-grain validation
   - Delivery-delay logic
   - Category translation coverage
   - Monthly trend readiness

4. **Business reporting — Power BI**
   - KPI-driven reporting
   - Sales and order trends
   - Category and seller performance
   - Delivery and customer-review analysis

## Repository Structure

```text
olist-data-analysis/
├── dashboard/
│   ├── olist_project.pbix
│   └── README.md
├── notebooks/
│   └── Olist_Project_updated.ipynb
├── sql/
│   ├── schema.sql
│   ├── data_loading.sql
│   └── validation_queries.sql
├── .gitignore
└── README.md
```

### Why the datasets are not stored in this portfolio repository

The original Olist dataset contains multiple large CSV files, including a geolocation table with more than one million rows. Keeping full raw and generated CSVs in a portfolio repository adds unnecessary repository weight and makes the project harder to clone and review. GitHub also recommends keeping repositories small and warns that large tracked files can affect repository performance. citeturn1search0turn1search1

The notebook is therefore designed to work from a local `data/raw/` folder. Download the public Olist dataset separately and place the CSV files there before running the notebook.

## Getting Started

### 1. Download the Olist dataset

Download the **Brazilian E-Commerce Public Dataset by Olist** and place the source CSV files under:

```text
data/raw/
```

The notebook expects these files:

- `olist_orders_dataset.csv`
- `olist_order_items_dataset.csv`
- `olist_order_payments_dataset.csv`
- `olist_order_reviews_dataset.csv`
- `olist_customers_dataset.csv`
- `olist_sellers_dataset.csv`
- `olist_products_dataset.csv`
- `olist_geolocation_dataset.csv`
- `product_category_name_translation.csv`

### 2. Run the Python notebook

Open:

`notebooks/Olist_Project_updated.ipynb`

The notebook uses repository-relative paths, so it does not depend on a personal Windows/Desktop path.

### 3. Set up MySQL

Create the database and tables using:

`sql/schema.sql`

Then adapt the local file-loading path in:

`sql/data_loading.sql`

**Important:** database credentials and machine-specific paths are intentionally not stored in the repository.

### 4. Run validation

Execute:

`sql/validation_queries.sql`

The validation layer should be completed before interpreting dashboard KPIs.

### 5. Open the Power BI report

The Power BI report is available at:

`dashboard/olist_project.pbix`

See `dashboard/README.md` for the dashboard handoff notes.

## Key Analyst Skills Demonstrated

**Python:** Pandas, NumPy, data cleaning, type conversion, validation  
**SQL:** schema design, loading, joins, aggregations, data-quality checks  
**Power BI:** KPI reporting and business dashboard development  
**Analytics:** data grain, business-rule validation, trend analysis, reporting readiness  
**Workflow:** reproducible project structure, documentation, Git/GitHub

## Analyst Positioning

This project is designed to demonstrate an important analyst capability: **knowing whether a metric is trustworthy before presenting it to a stakeholder**.

Rather than positioning the work as a collection of charts, the repository emphasizes data quality, relational thinking, validation, and business-ready reporting.

## Project Status

**Portfolio-ready:** core Python preparation, MySQL schema/loading workflow, validation SQL, and Power BI report are included.

Future enhancements can focus on dashboard screenshots and a concise business-insights section rather than adding more raw data or unnecessary technical files.
