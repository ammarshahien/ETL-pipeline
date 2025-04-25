# ETL-pipeline

# Car Price Data Pipeline

A complete ETL pipeline for scraping car listings, processing the data, and loading it into BigQuery.

## Pipeline Overview

1. **Extract**: Scrape car listings from OpenSooq using `scrape_mongo.py`
2. **Load to Data Lake**: Store raw data in MongoDB
3. **Clean**: Clean and transform data with `clean_data_mongo.py`
4. **Load to Warehouse**: Transfer processed data to BigQuery using `data_trans.py`
5. **Orchestrate**: Manage the workflow with Apache Airflow

## Setup

1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Configure MongoDB and BigQuery in `config/config.json`
4. Place your BigQuery credentials in `credentials/`
5. Set up Airflow to run the DAGs

## Requirements

- Python 3.8+
- MongoDB
- Google Cloud BigQuery
- Apache Airflow

## Airflow DAGs

- `car_data_pipeline`: Main ETL workflow
- `file_management`: Setup and file management tasks
