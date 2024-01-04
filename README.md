# Azure Data Integration and Analysis for Housing Data

## Project Overview
This project involves extracting housing data via HTTP request and loading it into Azure Data Lake Storage Gen2. The data initially in comma-separated value (CSV) format is processed and transformed to clean and structured data using Azure Databricks with Spark and JDBC. The cleaned data is then loaded into an Azure SQL database. An Azure Data Factory pipeline is defined to automate the data extraction, transformation, and loading process.

## Components
- **Azure Data Lake Storage Gen2:** Used for storing raw housing data.
- **Azure Databricks:** Used for running Spark jobs to clean and transform data.
- **Azure SQL Database:** The final destination for the cleaned and structured housing data.
- **Azure Data Factory:** Contains the pipeline definition for the automation of the ETL process.

## Data Flow
1. **Data Extraction:** Data is extracted using an HTTP request and stored in Azure Data Lake Storage Gen2.
2. **Data Cleaning and Transformation:** Spark jobs on Azure Databricks clean the comma-separated raw data and transform it. The transformation includes data type corrections, filtering, and aggregation to suit the requirements of the Azure SQL Database.
3. **Data Loading:** The cleaned and transformed data is loaded into the Azure SQL Database using JDBC for further analysis and reporting.
4. **Pipeline Automation:** Azure Data Factory orchestrates the workflow of the above processes, ensuring a smooth and automated ETL pipeline.

## Files in the Repository
- `ResourceGroup.png` - Screenshot detailing the Azure resource group setup for this project.
- `DataFactory.png` - Screenshot showing the pipeline configuration in Azure Data Factory.
- `CleanData-MoveToDB.ipynb` - Jupyter notebook with Python code that uses JDBC and Spark for data cleaning and transformation.

## Prerequisites
- Azure subscription
- Access to Azure Data Lake Storage Gen2, Azure Databricks, Azure SQL Database, and Azure Data Factory
- Familiarity with Python, Spark, and JDBC

## Setup Instructions
1. **Azure Services Configuration:** Ensure that all Azure services are correctly set up and configured as shown in `ResourceGroup.png`.
2. **Data Extraction Configuration:** Configure the HTTP request to pull the latest housing data into Azure Data Lake Storage Gen2.
3. **Data Transformation Script:** Execute the `CleanData-MoveToDB.ipynb` notebook in Azure Databricks to clean and transform the data.
4. **Azure Data Factory Pipeline:** Set up the pipeline as per the configuration in `DataFactory.png` to automate the ETL process.


## Automation
The pipeline is scheduled to run automatically at defined intervals. However, it can also be triggered manually if needed.

## Contributing
Contributions to this project are welcome. Please refer to the contribution guidelines before making a pull request.

## License

MIT License

Copyright (c) 2024 Farhad Vadiee

## Contact
farhad.vadiee@gmail.com