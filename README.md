# GCP-Sales-Data-Analytics-Pipeline
A Scalable End-to-End Data Pipeline using Google Cloud Platform Services

This project showcases how to build a fully automated and scalable sales data analytics pipeline on Google Cloud Platform (GCP). From user-friendly data uploads to real-time dashboards, the architecture brings together multiple GCP services in a cohesive workflow tailored for data-driven decision-making.


# Key Features

    Python Flask Web Portal: Easy interface for uploading sales CSV files.

    Google Cloud Storage (GCS): Secure storage for uploaded files.

    Cloud Function (Serverless): Auto-triggered on file upload for processing.

    BigQuery Integration: Load and transform data into an analytical data warehouse.

    Looker Studio Dashboards: Visualize metrics with filtering and drill-down capabilities.

    Scalable Architecture: Fully serverless and event-driven, perfect for handling large datasets with minimal manual effort.


# Components and Services Used

    Flask Web App - Frontend to upload CSV files
    Google Cloud Storage (GCS) - Stores raw uploaded file
    Cloud Functions - Auto-triggers to parse and load data
    BigQuery - Stores and queries transformed data
    Looker Studio - Dashboard for visualization and reports
    Pub/Sub - For asynchronous processing (future scope)


# Step-by-Step Implementation

1. Web Portal Setup
   
       Developed with Python Flask.
       Provides a UI for users to upload sales .csv files.
       On upload, files are sent to a GCS Bucket.

2. Google Cloud Storage (GCS)
   
       Acts as a data lake for raw sales data.
       A bucket is created to store all incoming files.

3. Cloud Function (Trigger on GCS Upload)
   
       A Cloud Function is set up to listen for changes in the GCS bucket.
       When a file is uploaded:
         Parses the CSV file.
         Performs basic validations.
         Transforms fields (e.g., date parsing, formatting).
         Loads the processed data into a BigQuery table.

4. BigQuery Data Warehouse

       Structured table schema in BigQuery.
       Stores cleaned and structured data.
       Enables powerful SQL queries and joins.

5. Looker Studio Dashboard

       Connected to BigQuery as the data source.
       Interactive dashboard with:
         Sales summaries
         Monthly trends
         Top-performing products
         Region-wise sales
         Filter and drill-down features

# Deployment Considerations

Make sure GCP services like Cloud Functions, BigQuery, and GCS are enabled in your project.

Secure GCS and BigQuery with IAM permissions.

Use Cloud Scheduler or Pub/Sub for scheduling or expanding automation.

Monitor with Cloud Logging and Error Reporting.
   
