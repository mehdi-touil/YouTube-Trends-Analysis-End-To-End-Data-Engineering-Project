# YouTube Trends Analysis: End-to-End Data Engineering Project

This project aims to analyze trending videos across different regions using the AWS ecosystem and build a Power BI dashboard to answer key questions about video popularity factors.

## Project Overview

- **Data Engineering Lifecycle:**
  - The project follows a comprehensive data engineering lifecycle, encompassing data extraction, transformation, loading, and analysis.

- **Dataset:**
    - The dataset includes several months of data on daily trending YouTube videos from regions including the US, GB, DE, CA, FR, RU, MX, KR, JP, and IN. The dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/datasnaek/youtube-new/).
- **Architecture:**
![architecture loading](Architecture.jpeg)

## Key Project Steps

1. **Introduction:**
   - Overview of the project and its importance.

2. **Learning Objectives:**
   - Explain Factors that make a video popular.

3. **Understanding the Dataset:**
   - Exploration of the dataset used in the project.

4. **Data Processing:**
   - AWS Glue 
   - AWs Lambda

5. **AWS Services Utilized:**
   - Creation of IAM accounts and installation of AWS CLI.
   - Setting up an S3 bucket and uploading data.
   - Implementation of a Data Lake using Glue Crawler and Catalog.

6. **Querying and Analysis:**
   - Use of Athena and SQL for querying data.
   - Solving errors and preprocessing data.
   - Writing ETL jobs in Lambda for data cleaning.

7. **AWS Lambda and Layers:**
   - Understanding AWS Lambda and layers in the context of the project.

8. **Dashboard Creation:**
   - Querying cleaned data on Athena and visualizing it on Power BI.

## Data Engineering Lifecycle
1. **Data Lake Storage:**
   - Store Our Data to S3 Bucket.

1. **Data Processing and ETL:**
   - Trigger our  Aws lambda to Transforn Our Json files and clean them and store them in parquet format and  create a table to be queried in Athena.
   - Convert Our CSv Files to parquet and clean them and store them in a Table and Query in Athena.
   - All scripts are in scripts folder.

3. **Build Analytical Data:**
   - Use ETL Job to join our cleaned Tables for Writing final analytics table data to S3, partitioned by category_id.
3. **Build Dashboard using PowerBI:**
   - Build a dashboard in powerBi using ODBC as DataSource.
![Dashboard](Images/dashboard.png)

# AWS Services UsedSed

## Amazon S3
Amazon S3 is an object storage service providing manufacturing scalability, data availability, security, and performance.
## AWS IAM
AWS Identity and Access Management (IAM) is a service enabling us to manage access to AWS services and resources securely.

## AWS Glue
AWS Glue is a serverless data integration service that simplifies the discovery, preparation, and combination of data for analytics, machine learning, and application development.

## AWS Lambda
AWS Lambda is a computing service that allows programmers to run code without creating or managing servers.

## AWS Athena
AWS Athena is an interactive query service for S3 that eliminates the need to load data; it stays in S3.
