# Practice Project – ETL GDP Data Pipeline

## Overview

This project demonstrates the development of an end-to-end Extract, Transform and Load (ETL) pipeline using Python.

The pipeline extracts Gross Domestic Product (GDP) data from an archived International Monetary Fund (IMF) webpage, transforms the values from millions to billions of USD, exports the processed data as CSV and JSON files, loads the data into a SQLite database, and validates the results using a SQL query.

This project was completed as part of the IBM Data Engineering Professional Certificate to practise core data engineering concepts.

---

## Project Objectives

The ETL pipeline performs the following tasks:

- Extract GDP data from a public web source.
- Transform GDP values from millions to billions of USD.
- Export the transformed data as CSV and JSON files.
- Load the data into a SQLite database.
- Execute a SQL query to validate the loaded data.
- Log each stage of the ETL process.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Requests
- BeautifulSoup (bs4)
- SQLite3
- Jupyter Notebook
- Visual Studio Code

---

## Project Structure

```text
practice-project-etl-gdp-data/
│
├── .gitignore
├── Countries_by_GDP.csv
├── Countries_by_GDP.json
├── etl_project_gdp.ipynb
├── etl_project_gdp.py
├── etl_project_log.txt
├── README.md
├── requirements.txt
└── World_Economies.db
```

---

## ETL Workflow

### Extract

- Retrieve GDP data from the archived IMF webpage.
- Parse the HTML using BeautifulSoup.
- Store the extracted data in a pandas DataFrame.

### Transform

- Convert GDP values from millions to billions of USD.
- Round GDP values to two decimal places.
- Rename the GDP column.

### Load

- Export the transformed dataset as:
  - CSV
  - JSON
- Load the transformed data into a SQLite database table named **Countries_by_GDP**.

### Validate

Run the following SQL query to retrieve countries with a GDP greater than or equal to 100 billion USD.

```sql
SELECT *
FROM Countries_by_GDP
WHERE GDP_USD_billions >= 100;
```

---

## Outputs

The project generates the following files:

| File | Description |
|------|-------------|
| Countries_by_GDP.csv | GDP dataset exported as CSV |
| Countries_by_GDP.json | GDP dataset exported as JSON |
| World_Economies.db | SQLite database containing the transformed data |
| etl_project_log.txt | Execution log of the ETL pipeline |

---

## Skills Demonstrated

- ETL Pipeline Development
- Web Scraping
- Data Extraction
- Data Transformation
- Data Cleaning
- CSV and JSON Export
- SQLite Database Integration
- SQL Querying
- Python Functions
- Process Logging

---


## Acknowledgements

This project was completed as part of the IBM Data Engineering Professional Certificate and has been adapted as a personal portfolio project.