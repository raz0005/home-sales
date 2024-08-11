
# Home Sales Data Analysis using PySpark

## Overview

This project utilizes PySpark to analyze home sales data to identify key metrics about home sales. The analysis includes creating temporary views, partitioning data, caching tables, and comparing query runtimes. By leveraging the power of PySpark, we can efficiently process and analyze large datasets, making this approach scalable and applicable to real-world scenarios.

## Requirements

Ensure you have the following software installed:

- **Google Colab**
- **Java**
- **Apache Spark**
- **PySpark**

Set up your environment by configuring the necessary environment variables for Spark.

## Data Analysis Workflow

1. **Data Ingestion**: 
   - Read the dataset into a Spark DataFrame.

2. **Temporary View Creation**:
   - Create temporary SQL views from the DataFrame to facilitate SQL query execution.

3. **SQL Queries**:
   - Write and execute various SQL queries to calculate key metrics:
     - Average price for four-bedroom homes sold each year.
     - Average price of homes with three bedrooms and three bathrooms per year built.
     - Average price of homes with specific criteria (three bedrooms, three bathrooms, two floors, and ≥2,000 square feet) per year built.
     - Average home price per "view" rating, filtered for prices ≥ $350,000, with runtime tracking.

4. **Caching**:
   - Cache the temporary view and validate the cache.
   - Run the SQL query on the cached data and compare the runtime with the non-cached query.

5. **Data Partitioning**:
   - Partition the data by the "date_built" field and save it as Parquet format.
   - Load the Parquet data and create a new temporary view for further analysis.

6. **Performance Comparison**:
   - Compare the query runtimes between the original, cached, and Parquet partitioned data.

7. **Uncaching**:
   - Uncache the temporary view and verify.

## Conclusion

This analysis demonstrates how PySpark can be used to efficiently process and analyze large datasets. By caching and partitioning data, query runtimes can be significantly reduced, leading to better performance. This scalable approach can be applied to larger datasets in real-world scenarios, making it a valuable technique for big data analytics.

## How to Run

1. **Set Up Environment**: Ensure that your environment is configured with Java, Apache Spark, and PySpark.
2. **Clone Repository**: Clone this GitHub repository to your local machine or Google Colab.
3. **Run the Notebook**: Follow the instructions in the Jupyter Notebook or Python script provided in the repository.
4. **Review Outputs**: Examine the output of each step to understand the data processing and analysis workflow.


