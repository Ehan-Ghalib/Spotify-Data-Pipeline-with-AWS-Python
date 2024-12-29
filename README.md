# Build Scalable Data Engineering Pipeline with API Integration on AWS Using Python

## Project Overview

Designed and implemented a cloud-native data pipeline to ingest, transform, and analyze Spotify playlist data for the Top 100 songs. The pipeline leverages Amazon Web Services (AWS) to ensure scalability, automation, and efficiency.

## Architecture Diagram

![Data Pipeline Architecture Diagram](https://github.com/Ehan-Ghalib/Spotify-Data-Pipeline-with-AWS-Python/blob/ade0ca3e8ba7a26d5967d6ea0e8c6570a10ee2c4/Spotify%20AWS-Python%20Pipeline%20Diagram.png)

## Key Components

### Data Ingestion

- A CloudWatch-triggered AWS Lambda function extracts data from the Spotify API for the Top 100 playlist.
- The function loads raw JSON data into an S3 bucket for further processing.

### Data Transformation

- An S3 trigger initiates a second Lambda function, which parses and transforms the raw data into structured datasets for artists, albums, and tracks.
- These transformed datasets are saved in dedicated folders within S3.

### Data Cataloging and Analysis

- AWS Glue Crawler automatically catalogs the transformed data, creating metadata in the Glue Data Catalog.
- Amazon Athena enables querying and analyzing the cataloged data, providing insights directly from S3 without requiring ETL to a traditional database.

## Outcomes

- Created structured datasets for artists, albums, and tracks, enabling further analysis.
- Leveraged serverless architecture to achieve cost-efficiency and automated scaling.
- Enabled end-to-end data flow and seamless querying of music data using Athena, removing the need for manual intervention.

This project demonstrates how AWS services can be integrated to build robust data pipelines and analyze data efficiently. It highlights practical applications of serverless computing, data transformation, and cloud-based analytics in real-world use cases.
