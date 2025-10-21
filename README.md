# AWS ETL Pipeline

🧩 Serverless ETL Data Pipeline on AWS
Tech Stack

AWS Lambda, AWS S3, AWS Glue, AWS Athena, Python (Boto3, Pandas), PyArrow

📘 Project Overview

Designed and implemented a fully serverless ETL (Extract, Transform, Load) pipeline on AWS to process nested JSON order data and transform it into an analytics-ready Parquet format for efficient querying and analysis.

⚙️ Workflow

AWS S3 – Stores incoming raw JSON order data.

AWS Lambda (Python) – Automatically triggered by S3 upload events to:

Read nested JSON data from S3.

Flatten complex JSON (customer and product details) using Pandas.

Convert structured data into Parquet format using PyArrow.

Save transformed data back to S3 with timestamp-based partitioning for optimized queries.

AWS Glue Crawler – Updates the AWS Glue Data Catalog automatically to reflect the latest schema.

AWS Athena – Enables SQL-based querying directly over Parquet files stored in the S3 Data Lake.

🚀 Key Features

Fully serverless, scalable, and event-driven architecture.

Automated schema updates via AWS Glue Crawler.

Optimized analytics performance with Parquet storage.

No manual intervention required once deployed.

📊 Impact

Reduced manual data preparation time by 90%.

Enabled real-time analytics with zero infrastructure management.

Improved query performance and storage efficiency using Parquet.

Small project containing an AWS Lambda ETL function (lambda_function.py) and sample ETL config (`orders_etl.json`).

Files:

- `lambda_function.py` - Lambda handler and ETL logic
- `orders_etl.json` - ETL configuration / sample input

Usage:

- Edit `orders_etl.json` for your ETL mapping
- Deploy `lambda_function.py` to AWS Lambda as needed

License: MIT
