# Python ETL Pipeline

A Python-based ETL (Extract, Transform, Load) pipeline that extracts car data from CSV, JSON, and XML files, transforms the data, and loads the result into a CSV file.

## Project Overview

This project demonstrates the basic ETL process using Python and Pandas.

The pipeline performs three main stages:

1. **Extract** – Reads data from CSV, JSON, and XML files.
2. **Transform** – Rounds car prices to two decimal places.
3. **Load** – Saves the transformed data into a CSV file.

The project also maintains a log file to track the progress of each ETL stage.

## Technologies Used

* Python 3
* Pandas
* XML ElementTree
* Glob
* Git & GitHub

## Project Structure

```text
python-etl-pipeline/
│
├── test.py
├── datasource.zip
├── log_file.txt
├── transformed_data.csv
├── requirements.txt
└── README.md
```

## Data Sources

The pipeline supports the following file formats:

* CSV
* JSON
* XML

The extracted data contains the following fields:

* `car_model`
* `year_of_manufacture`
* `price`
* `fuel`

## ETL Process

### 1. Extract

The `extract()` function searches the project directory for CSV, JSON, and XML files and combines their contents into a Pandas DataFrame.

### 2. Transform

The `transform()` function rounds the `price` column to two decimal places.

```python
data['price'] = data['price'].round(2)
```

### 3. Load

The `load_data()` function saves the transformed DataFrame as:

```text
transformed_data.csv
```

### 4. Logging

The `log_progress()` function records the progress of the ETL process in:

```text
log_file.txt
```

The log records events such as:

```text
ETL Job Started
Extract phase Started
Extract phase Ended
Transform phase Started
Transform phase Ended
Load phase Started
Load phase Ended
ETL Job Ended
```

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/python-etl-pipeline.git
```

Navigate to the project directory:

```bash
cd python-etl-pipeline
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the virtual environment.

### Windows PowerShell

```powershell
.\.venv\Scripts\Activate.ps1
```

### Linux/macOS

```bash
source .venv/bin/activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Running the Project

Run the ETL script:

```bash
python test.py
```

After execution, the pipeline generates:

```text
transformed_data.csv
log_file.txt
```

## Example Output

The transformed data contains:

| car_model | year_of_manufacture |    price | fuel   |
| --------- | ------------------: | -------: | ------ |
| Toyota    |                2020 | 25000.50 | Petrol |
| BMW       |                2021 | 45000.75 | Diesel |

## Requirements

The main external dependency is:

```text
pandas
```

Generate a `requirements.txt` file with:

```bash
pip freeze > requirements.txt
```

## Learning Objectives

This project demonstrates:

* Reading CSV files using Pandas
* Reading JSON files using Pandas
* Parsing XML files using ElementTree
* Combining multiple DataFrames
* Data transformation
* Rounding numerical values
* Writing data to CSV
* Python virtual environments
* Basic ETL pipeline design
* Logging ETL processes
* Using Git and GitHub

## License

This project is intended for educational and learning purposes.
