# Big-Data-ETL

# Overview

I performed an ETL process in the cloud and uploaded a DataFrame to an RDS instance as part of an assignment. The assignment involved analyzing Amazon's product review datasets, which are publicly available and quite large. The Outdoor product datasets I chose has and over 2 million rows of data.  This much data makes data analysis very demanding on the average local computer. I used PySpark to perform a statistical analysis of selected data to help conduct ETL. 


# Extract

Using pyspark, I imported the S3 bucket and wrote the .gz file into a dataframe. 

![1677778428200](image/README/1677778428200.png)

# Transform

I tranformed the original dataframe into three dataframes that will be imported into SQL database, ensuring that each table had a common column to support primary and foriegn key connections.

I converted string data to int and datetype as needed. 

![1677781560554](image/README/1677781560554.png)

Review ID Dataframe

![1677778840716](image/README/1677778840716.png)

Product ID Dataframe

![1677778748179](image/README/1677778748179.png)

Customers Dataframe

![1677778762238](image/README/1677778762238.png)

Vine Dataframe

![1677778778132](image/README/1677778778132.png)

# Load

After the dataframes are complete, I can load them to the AWS RDS PostgresSQL dabase called "my_data_class_db"

![1677779046353](image/README/1677779046353.png)
