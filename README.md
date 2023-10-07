## Web Scraping of Nike Website to create a repository of weekly featured show collection for men.

## Overview
The goal is to build an ETL pipeline using the data scraped from Nike website on AWS. The pipeline will rerieve data from Nike website, transform it to a desired format and load it into AWS data store.

## Process
ETL Process Overview
-Extract data by web scraping data from Nike website using the beatifulsoup python library
-Deploy the data extraction code using the Lambda function -Run trigger using EventBridge to automate data extraction every Friday at 6 pm 
-Make the necessary transformations to the data
-transformed data is saved in the nik-web-scrapping-project/Nike_data in the S3 bucket
-Glue crawler will infer schema when new data arrives in the in the Nike_data folder
-Data catalog manage metadata repository 
-Query S3 data using Athena

