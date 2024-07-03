# ETL-Country-GDP-Data-Processing

## Project Overview

This project involves creating a complete ETL (Extract, Transform, Load) pipeline to process data on the largest banks by market capitalization. The data is extracted from a Wikipedia page, transformed to include market capitalization in multiple currencies, and loaded into both a CSV file and a SQLite database.

## Table of Contents

- Project Overview
- Data Source
- Project Structure
- Setup and Installation
- Usage
- Functions
- Logging
- License

## Data Source

The data is sourced from the Wikipedia page listing the largest banks by market capitalization:
- List of largest banks

## Project Structure

ETL-Country-GDP-Data-Processing <br />
├── exchange_rate.csv <br />
├── Largest_banks_data.csv <br />
├── Banks.db <br />
├── code_log.txt <br />
├── etl_script.py <br />
└── README.md


## Setup and Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/ETL-Country-GDP-Data-Processing.git
    cd ETL-Country-GDP-Data-Processing
    ```

2. Install the required libraries:
    ```bash
    pip install requests pandas numpy beautifulsoup4
    ```

## Usage

Run the ETL script:
```bash
python etl_script.py
```
## Functions

### `log_progress(message)`
Logs the progress of the ETL process to a log file.

### `extract(url, table_attribs)`
Extracts data from the specified URL and returns a DataFrame.

### `transform(df, csv_path)`
Transforms the extracted data by adding columns for market capitalization in GBP, EUR, and INR.

### `load_to_csv(df, output_path)`
Saves the transformed data to a CSV file.

### `load_to_db(df, sql_connection, table_name)`
Loads the transformed data into a SQLite database table.

### `run_query(query_statement, sql_connection)`
Executes a SQL query on the database and prints the results.

## Logging

The ETL process logs its progress to `code_log.txt` with timestamps for each stage.

## License

This project is licensed under the MIT License.
