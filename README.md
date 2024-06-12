# Zillow-Data-Pipeline

Welcome to the Zillow Real Estate Data ETL Project! This project demonstrates how to build and automate a Python ETL (Extract, Transform, Load) process using various AWS services and Apache Airflow.

## Project Overview

This project aims to extract real estate data from the Zillow Rapid API, load it into an Amazon S3 bucket, transform it using AWS Lambda functions, and finally load it into Amazon Redshift for visualization using Amazon QuickSight.

Key components of the project include:

- **Python ETL Pipeline**: Automates the extraction, transformation, and loading of data.
- **AWS Services**: Uses S3, Lambda, Redshift, and QuickSight for cloud-based data storage, transformation, and visualization.
- **Apache Airflow**: Orchestrates the ETL workflow and manages data pipelines.

## Architecture

**Data Extraction**: Extract real estate data from Zillow Rapid API using a Python script.

**Data Loading**: Load the extracted data into an Amazon S3 bucket.

**Data Transformation**: Trigger a series of AWS Lambda functions to transform the data.

Data Storage****: Store the transformed data back into a different S3 bucket in CSV format.

**Data Loading to Redshift**: Use Apache Airflow to monitor the S3 bucket for the transformed data using an S3KeySensor operator and load it into Amazon Redshift.

**Data Visualization**: Connect Amazon QuickSight to the Redshift cluster to visualize the data.

![Data Pipeline Architecture](./images/Data%20Pipeline%20Architecture.png)
*Figure 1. Data Pipeline Architecture*

## Data Pipeline Details

- Extract: The ETL script fetches data from the Zillow Rapid API.
- Load: Data is loaded into an S3 bucket as raw data.
- Transform: Lambda functions process the raw data and save the transformed data in another S3 bucket.
- Load to Redshift: Apache Airflow monitors the transformed data bucket and loads the data into Redshift.
- Visualization: QuickSight connects to Redshift for data visualization.

## Visualization
Use Amazon QuickSight to create interactive dashboards and visualizations based on the Zillow real estate data.

## Contributing
We welcome contributions! Please fork this repository and create a pull request with your changes. Ensure you follow best practices and include necessary tests.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements
- Thanks to *Zillow* for providing the API.
- Thanks to *AWS* for cloud services.
- Thanks to the *Apache Airflow* community for workflow orchestration tools.