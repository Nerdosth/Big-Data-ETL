# Amazon Outdoors Reviews ETL

# Overview

This project demonstrates the Extract, Transform, Load (ETL) process using PySpark and PostgreSQL using Google Colab. The data used in this project are Amazon Reviews of US Outdoor products.

## Requirements

* Google Colab
* PySpark
* PostgreSQL

## Setup

1. Make sure you have a Google Colab environment available.
2. Install Spark, and PostgreSQL JDBC driver.
3. Set up the environment variables for Java and Spark.

## Extraction

1. Read the Amazon Reviews of US Outdoor data from an S3 Bucket as a Spark DataFrame.
2. Display the DataFrame and schema.

![1677778428200](image/README/1677778428200.png)

# Transformation

1. Cast columns to appropriate data types.
2. Create tables: review_id_table, products, customers, and vine_table.
3. Drop duplicates and perform any necessary column renaming.

![1677781560554](image/README/1677781560554.png)

Review ID Dataframe

![1677778840716](image/README/1677778840716.png)

Product ID Dataframe

![1677778748179](image/README/1677778748179.png)

Customers Dataframe

![1677778762238](image/README/1677778762238.png)

Vine Dataframe

![1677778778132](image/README/1677778778132.png)

# Loading

1. Configure settings for PostgreSQL RDS.
2. Load data from the transformed DataFrames into their respective tables in PostgreSQL RDS.

![1677779046353](image/README/1677779046353.png)


## Conclusion

In this project, a successful ETL process was implemented using PySpark to extract data from Amazon Reviews of US Outdoor products, transform the data, and load it into a PostgreSQL database. The demonstration covered working with Spark DataFrames and connecting to a PostgreSQL RDS instance to store the transformed data. This project showcases the power and flexibility of PySpark in handling large datasets and its interoperability with other data storage solutions like PostgreSQL. The ETL pipeline can be further improved and adapted to handle different data sources and transformations as needed.
