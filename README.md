# SparkSQL Data Analysis with PySpark

This project demonstrates the use of PySpark's SparkSQL module to perform data analysis tasks on a dataset containing home sales information. The analysis involves querying and manipulating the data using SparkSQL queries to answer specific questions. The code showcases how to install Spark, load data from an external source, create temporary views, and perform various SQL-like operations.

## Table of Contents
- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Data Analysis](#data-analysis)
- [Questions](#questions)
- [Conclusion](#conclusion)

## Introduction
This project utilizes Apache Spark's PySpark library to analyze a dataset of home sales. The code demonstrates how to perform various data analysis tasks using SparkSQL, including filtering, grouping, and aggregating data.

## Getting Started
To run the code in this project, you'll need to have Spark, Java, and Python installed on your system. The code is designed to run in a Jupyter Notebook environment. Here are the basic steps to get started:

1. Set the desired Spark version in the `spark_version` variable in the code.
2. Install Java and Spark dependencies using the provided code snippet.
3. Import necessary libraries and initialize a SparkSession.
4. Load the dataset from an external source (AWS S3 bucket) and create a temporary view.

## Data Analysis
The following questions are addressed using SparkSQL queries:

1. What is the average price for a four-bedroom house sold in each year, rounded to two decimal places?
2. What is the average price of a home for each year the home was built, having 3 bedrooms and 3 bathrooms, rounded to two decimal places?
3. What is the average price of a home for each year built that has 3 bedrooms, 3 bathrooms, with two floors, and is greater than or equal to 2,000 square feet, rounded to two decimal places?
4. What is the "view" rating for the average price of a home, rounded to two decimal places, where the homes are greater than or equal to $350,000? This query also measures the runtime of the query:
   - Initially ran in 1.14 seconds.
   - After caching the table and rerunning, the time was brought down to 0.766 seconds.
   - By partitioning and using Parquet format, the runtime was further reduced to 0.597 seconds.
5. Caching the `home_sales` temporary table and checking if it's cached.
6. Running the same query as in Question 4 using the cached data and comparing the runtime with the uncached version.
7. Partitioning the data by the `date_built` field and writing it in Parquet format.
8. Reading the Parquet-formatted data and creating a temporary table.
9. Running the same query as in Question 4 using the Parquet DataFrame and comparing the runtime with the cached version.
10. Uncaching the `home_sales` temporary table.
11. Checking if the `home_sales` table is no longer cached.

## Conclusion
This project showcases how to leverage PySpark's SparkSQL module for data analysis tasks on a home sales dataset. By executing SparkSQL queries, the code demonstrates how to answer specific questions and compare the performance of different approaches, such as caching and using Parquet format. This README provides an overview of the project and its functionality.

I utilized a recorded instructor review of this analysis to troubleshoot problems and verify the accuracy of this project.

