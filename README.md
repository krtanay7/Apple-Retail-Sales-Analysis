# Apple Retail Sales Analysis

A focused SQL analysis of Apple retail sales data (dataset of ~1M+ rows). The repository contains data creation scripts, table definitions, and analytical SQL queries used to answer business questions about sales, product trends, store performance, and warranty claims.

Table of Contents
- Project overview
- Repository structure
# Apple Retail Sales Analysis

A focused SQL analysis of Apple retail sales data (dataset of ~1M rows+). This repository contains the SQL schema, analytical queries, and a Python data-generation script used to produce the CSV datasets.

## Repository structure
- `Table_creation.sql` — SQL to create the database schema and (optionally) load CSVs into tables.
- `SQL_QUERIES.sql` — Analytical queries used to answer business questions.
- `Dataset/Apple Data Set Creation Using PYTHON.py` — Python script to generate sample CSV datasets.
- `Dataset/*.csv` — CSV files used by the analysis: `category.csv`, `products.csv`, `sales.csv`, `stores.csv`, `warranty.csv`.
- `requirements.txt` — Minimal Python dependencies for regenerating the dataset.

## Prerequisites
- Python 3.8 or newer
- `pip`

Install dependencies:

```powershell
python -m pip install -r requirements.txt
```

The `requirements.txt` in this repo currently lists:

- `pandas`
- `Faker`

Pin versions if you need strict reproducibility (optional).

## Reproduce / regenerate the CSV files
1. Open a terminal and change into the project root.
2. Install dependencies (see above).
3. Run the data-generation script from the project root so paths resolve correctly:

```powershell
cd Dataset
python "Apple Data Set Creation Using PYTHON.py"
```

The script will generate CSV files (categories, products, stores, sales, warranty) in the current directory. Move them into `Dataset/` if you ran the script from another location.

## How to run the SQL analysis
1. Create a database (Postgres, MySQL, SQLite, etc.) and open a SQL client.
2. Run `Table_creation.sql` to create the tables and import CSV data.
3. Open and run the queries from `SQL_QUERIES.sql` to reproduce the analyses.

Notes:
- `Table_creation.sql` defines tables: `stores`, `category`, `products`, `sales`, and `warranty`.
- Use your database's recommended bulk-import method (e.g., `COPY` for Postgres, `LOAD DATA` for MySQL).

## Validation & next steps
- I created a `requirements.txt` with the dataset dependencies.
- If you'd like, I can run the Python script here to validate the CSV outputs (requires the environment to have Python and pip available).
- I can also pin package versions in `requirements.txt` for reproducible installs.

## Contact
If you have questions or want help running the analysis, open an issue or contact the repository owner.
