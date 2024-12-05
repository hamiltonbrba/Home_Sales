# Home Sales Analysis with PySpark

## Overview
This project uses PySpark to analyze home sales data, leveraging SparkSQL, caching, and partitioning to optimize performance.

## Objectives
1. Analyze home sales data to extract key insights.
2. Improve query performance with caching and data partitioning.
3. Compare runtimes for uncached, cached, and partitioned queries.

## Dataset
- Source: AWS S3  
- File: `home_sales_revised.csv`  
- Features: Bedrooms, bathrooms, price, square footage, year built, view ratings.

## Steps
1. Initialize Spark and load the dataset.
2. Create a temporary SQL view for querying.
3. Run queries to calculate:
   - Average price for 4-bedroom houses by year.
   - Average price of homes (3 beds, 3 baths) by year built.
   - Average price of homes (3 beds, 3 baths, 2 floors, ≥ 2,000 sq ft) by year built.
   - Average price per view rating (filter: price ≥ $350,000).
4. Cache the table and re-run queries to measure runtime improvements.
5. Partition the data by `date_built` and save as Parquet.
6. Run queries on the partitioned data and compare runtimes.

## Technologies
- **Apache Spark 3.4.0**
- **PySpark**
- **Parquet** for storage optimization
- **Python 3.8+**

## How to Run
1. Clone this repository:
   ```bash
   git clone <https://github.com/hamiltonbrba/Home_Sales.git>
   cd <Home_Sales>
   ```
2. Install dependencies and set up Spark.
3. Run the notebook or Python script.
