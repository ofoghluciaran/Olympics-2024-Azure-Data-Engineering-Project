# Olympics 2024 Azure Data Engineering Project
# Azure Data Engineering Project

## Overview

This repository showcases an end-to-end Azure Data Engineering project. It demonstrates the workflow of ingesting, transforming, and exporting data using Azure Data Factory, Spark, and Databricks. The project includes a Databricks notebook detailing each step in the data pipeline.

## Project Workflow

1. **File Upload:**
   - Data files are uploaded to GitHub and then moved to an Azure Data Factory (ADF) container for processing.

2. **Storage Configuration:**
   - Mount Azure Data Lake Storage (ADLS) Gen2 in Databricks using OAuth authentication to securely access the data.

3. **Data Ingestion:**
   - Data is ingested from CSV files stored in the ADF container into Spark DataFrames.
   - Temporary SQL views are created for querying and manipulation.

4. **Data Transformation:**
   - SQL queries are used within Databricks to clean, transform, and enrich the data, preparing it for analysis.

5. **Data Export:**
   - The transformed data is saved back to ADLS Gen2 as CSV files for further use or analysis.

## Notebook

The project includes a Databricks notebook that performs the following tasks:
- **Data Loading:** Reads data from CSV files in the ADF container and creates temporary views.
- **Data Transformation:** Executes SQL queries to clean and transform the data.
- **Data Export:** Writes the transformed data back to ADLS Gen2.

The notebook is located in the `notebooks` directory of this repository.

## Getting Started

### Prerequisites

- An Azure account with access to Azure Data Lake Storage (ADLS) Gen2.
- An Azure Data Factory instance for managing data pipelines.
- A Databricks workspace for running the notebook.
- Necessary permissions to mount storage, access data, and manage resources in Azure.
