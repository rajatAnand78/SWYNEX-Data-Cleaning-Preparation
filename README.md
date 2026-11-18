# Olist E-Commerce Data Analytics Project

## Project Overview

This project focuses on analyzing Brazilian e-commerce data using Python, MySQL, and Power BI.

The objective is to transform raw e-commerce data into clean, structured, and meaningful information that can help understand business performance, customer behavior, product sales, seller performance, payment patterns, and delivery operations.

The project follows an end-to-end data analytics workflow, starting with data cleaning in Python, followed by database integration in MySQL, SQL-based analysis, and interactive dashboard development in Power BI.

## Technologies Used

- Python
- Pandas
- NumPy
- Jupyter Notebook
- MySQL
- SQL
- Power BI
- Git and GitHub

## Dataset Information

The project uses the Brazilian E-Commerce Public Dataset by Olist.

The dataset contains information about customers, orders, products, sellers, payments, reviews, and geographical locations.

It consists of 9 datasets:

| Dataset | Records |
|---|---:|
| Customers | 99,441 |
| Orders | 99,441 |
| Order Items | 112,650 |
| Order Payments | 103,886 |
| Order Reviews | 99,224 |
| Products | 32,951 |
| Sellers | 3,095 |
| Geolocation | 738,332 |
| Category Translation | 71 |

**Total records: 1,299,091**

## Project Workflow

### 1. Data Cleaning Using Python

All nine datasets were independently cleaned using Pandas.

The cleaning process included:

- Understanding dataset structure and data types.
- Identifying missing values.
- Checking and handling duplicate records.
- Converting date columns into appropriate datetime formats.
- Identifying unusual and inconsistent values.
- Standardizing column names and text values.
- Investigating data-quality issues.
- Exporting cleaned datasets into CSV files.

Data was preserved wherever an anomaly could not be confidently classified as invalid.

### 2. Database Integration Using MySQL

Created a MySQL database named `olist_analysis`.

Loaded all nine cleaned CSV datasets into separate MySQL tables using Python and SQLAlchemy.

Database tables:

- customers
- orders
- order_items
- order_payments
- order_reviews
- products
- sellers
- geolocation
- category_translation

Verified the record counts after loading.

### 3. Database Relationships

Established primary keys and foreign-key relationships to maintain relational database integrity.

Relationships established:

- Customers → Orders
- Orders → Order Items
- Orders → Order Payments
- Orders → Order Reviews
- Products → Order Items
- Sellers → Order Items

Investigated unmatched product categories and identified 13 product records belonging to two categories that were not available in the category translation table. These records were preserved.

### 4. SQL Data Analysis

**In Progress**

Planned analysis includes:

- Sales and revenue analysis.
- Customer behavior analysis.
- Product performance analysis.
- Seller performance analysis.
- Payment analysis.
- Order and delivery analysis.
- Customer review analysis.

SQL JOINs, aggregations, subqueries, and window functions will be used to answer business questions.

### 5. Power BI Dashboard

**Planned**

The cleaned and analyzed data will be used to develop interactive Power BI dashboards to communicate important business insights through KPIs, charts, and visualizations.

## Project Folder Structure

```text
Olist_Data_Cleaning/
│
├── Raw_Data/
│
├── Cleaned_Data/
│
├── data_cleaning.ipynb
│
└── README.md
```

## Key Learning Outcomes

Through this project, I am developing practical skills in:

- Data cleaning and preprocessing using Python.
- Exploratory data analysis.
- Relational database design.
- Loading large datasets into MySQL.
- SQL primary keys and foreign keys.
- SQL JOINs and business analysis.
- End-to-end data analytics workflows.

## Project Status

- [x] Data cleaning using Python
- [x] Exporting cleaned datasets
- [x] MySQL database creation
- [x] Loading all nine datasets
- [x] Record count verification
- [x] Establishing database relationships
- [ ] SQL data integration and business analysis
- [ ] Power BI dashboard development
- [ ] Final project documentation

## Author

Developed as a hands-on Data Analytics portfolio project.