# Unemployment in India: Exploratory Data Analysis

A data analysis project performing data preprocessing, cleaning, and exploratory data analysis (EDA) on the Unemployment in India dataset.

## Overview

This project analyzes employment and unemployment trends across various states and regions in India. It performs necessary data cleaning procedures—such as handling missing values, stripping unwanted whitespace, and reformatting date variables—to produce a structured dataset for temporal and regional comparative analysis.

## Dataset & Features

The raw data is loaded from `Unemployment in India.csv`. The dataset includes the following attributes:

 Region: State/Territory in India
  Date: Reporting date for the metrics
  Frequency: Data collection frequency (e.g., Monthly)
  Estimated Unemployment Rate (%): Percentage of the labor force that is unemployed
  Estimated Employed: Estimated number of employed individuals
  Estimated Labour Participation Rate (%)**: Percentage of the working-age population in the labor force
  Area: Geographic area classification (Rural vs. Urban)
  Month: Extracted month name from the date
* **Year**: Extracted year from the date

---

## Project Workflow

### 1. Data Preprocessing
* Cleaned column names by stripping extra leading and trailing whitespace.
* Inspected dataset structure using `.info()`, `.describe()`, and `.shape`.

### 2. Data Cleaning
* Identified 28 completely empty/null rows across all columns.
* Dropped all 28 null rows (`.dropna()`) and reset the DataFrame index.
* Checked for duplicate entries (0 duplicate rows found).
* Verified zero null values remained across the dataset.
* Converted the `Date` column to proper datetime format (`%d-%m-%Y`).
* Feature Engineering: Derived `Month` and `Year` columns from the parsed `Date` variable.

### 3. Exploratory Data Analysis (EDA)
* Conducted initial data visualisations and summaries to observe distributions across states, areas (Rural/Urban), and time periods.

---

## Requirements & Environment

To run the notebook locally, ensure you have Python 3.x installed along with the following libraries:

```bash
pip install numpy pandas matplotlib seaborn
