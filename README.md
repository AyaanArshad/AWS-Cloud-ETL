# AWS Data ETL Pipeline with Glue and DataBrew
This repository provides a step-by-step guide on creating an AWS pipeline for data ETL using AWS Glue for data extraction from CSV, JSON, and XML files stored in an S3 bucket. Additionally, it includes a CI/CD pipeline for managing DataBrew recipes used to process extracted data and store it in Amazon Redshift and S3.
## Architecture
![image](https://user-images.githubusercontent.com/92472791/236751927-ed4e65cf-4d2f-4101-a9f8-7c2f283ac29a.png)

## Prerequisites
Before setting up the pipeline, make sure you have the following:

An AWS account with necessary permissions to create resources.
An S3 bucket to store your input data files and output data.
Access to AWS Glue and AWS DataBrew services.

## Steps
### 1. Setting up the Glue Data Catalog

The Glue Data Catalog is used to store metadata about the data sources and targets for the ETL process. Follow the tutorial here to set up the Glue Data Catalog.

### 2. Creating an S3 Bucket
Create an S3 bucket to store your input data files and output data. You can follow the instructions here to create an S3 bucket.

### 3. Creating a Glue ETL Job
Create a Glue ETL job to extract data from CSV, JSON, and XML files. Follow the steps outlined in this tutorial to create a Glue ETL job.

### 4. Configuring Glue Crawler
Set up a Glue crawler to discover and catalog the data in your S3 bucket. This crawler will update the Glue Data Catalog with metadata about your data files. Refer to this guide for instructions on creating a Glue crawler.

### 5. Creating CI/CD Pipeline for DataBrew Recipes
Create a CI/CD pipeline using AWS CodePipeline and AWS CodeBuild to manage your DataBrew recipes. This pipeline will enable version control, automated testing, and deployment of DataBrew recipes. Follow this tutorial to set up the CI/CD pipeline.
![image-databrew](https://user-images.githubusercontent.com/92472791/236751871-1cc7ab53-0431-474a-8e16-48c8be41a8ab.jpg)

### 6. Executing Glue ETL Job
Now that you have set up the pipeline and DataBrew recipes, trigger the Glue ETL job to extract data from CSV, JSON, and XML files using the following command:

`aws glue start-job-run --job-name <your-job-name>`

### 7. Monitoring and Troubleshooting
Monitor the progress and troubleshoot any issues that may arise during the ETL process. AWS Glue provides logs and metrics to assist with debugging. Refer to the AWS Glue documentation on monitoring and troubleshooting for more information.

## Helpful Resources!!
AWS Glue Developer Guide
AWS DataBrew Documentation
AWS Glue Samples and Templates
Feel free to reach out if you have any questions or need further assistance regarding my project!
