# Fabric-End_to_End-Pipeline-Project


## Project Summary – Microsoft Fabric End-to-End Data Engineering Architecture

This project demonstrates a multi-cloud end-to-end data engineering architecture with Microsoft Fabric as the primary platform, integrating Azure and AWS services to ingest, process, transform, store, and visualize data.

The architecture begins with Market A and Market B source systems, where data is generated in CSV format. The data is then routed through different cloud-based data engineering pipelines.


![image alt](https://github.com/oladebo/Fabric-End-to-End-Pipeline-Project/blob/2ab8cd70afb58b2a042882b88d2b21cab143cc79/Screen%20Shot%202026-08-25%20at%2022.56.21.png)

#### Key Architecture Flow


![image alt](https://github.com/oladebo/Fabric-End-to-End-Pipeline-Project/blob/20075490c2c99ee3cbf8b4068c0188b71951399b/Screen%20Shot%202026-08-25%20at%2022.56.52.png)

![image alt]()

![image alt]()

1. Data Ingestion

Data from Market A and Market B is received as CSV files.
Microsoft Fabric Data Factory is used to orchestrate data movement within the Fabric environment.
Azure Data Factory is also represented for Azure-based ingestion.
AWS Glue handles ingestion into the AWS environment.

2. Data Storage
The raw data is stored in different cloud storage platforms:

Microsoft OneLake – Fabric's centralized data lake.
Azure Blob Storage / ADLS Gen2 – Azure-based storage.
Amazon S3 – AWS-based data lake storage.

3. Data Processing
Different processing engines transform the raw data:

Microsoft Fabric Notebook with PySpark processes data stored in OneLake.
Databricks PySpark processes data from Azure Blob/ADLS Gen2.
Amazon EMR with PySpark processes data from Amazon S3.

These processes can perform activities such as data cleansing, transformation, validation, deduplication, and business-rule implementation.

4. Data Warehousing
The transformed data is loaded into analytical destinations:

Fabric SQL Database / Data Warehouse
Synapse Data Warehouse
AWS Redshift Data Warehouse

5. Data Modeling and Visualization
The processed data is brought together for semantic modeling, enabling business users to consume trusted and structured datasets.

Finally, Microsoft Power BI connects to the semantic model and provides dashboards and reports for business decision-making.

Business Scenario

One our client company operating in multiple markets across Africa. Market A and Market B generate daily sales, customer, product, and transaction data.

The company wants to answer questions such as:

- What are the sales trends across different markets?
- Which products generate the highest revenue?
- Which market is performing best?
- What are the daily and monthly sales volumes?
- How does customer behavior differ between markets?

The Fabric-based architecture provides a centralized way to ingest, transform, govern, model, and analyze this data, while still allowing the organization to consume data from Azure and AWS environments.





Main Objective

The main objective of this project is to demonstrate how Microsoft Fabric can be used to build a modern end-to-end data engineering solution, using OneLake, Data Factory, Notebooks/PySpark, Lakehouse/Warehouse, semantic models, and Power BI, while integrating with Azure and AWS data platforms.

In simple terms:

Sources → Fabric Data Factory → OneLake → PySpark Transformation → Lakehouse/Warehouse → Semantic Model → Power BI

with Azure and AWS integrated as additional data sources and processing/storage environments.

However this project a strong example of a modern hybrid/multi-cloud data engineering architecture using Microsoft Fabric as the central analytics platform.


Thanks,

Oladebo Ayanniyi (Data Engineer)












https://drive.google.com/file/d/1jVzCkc6KL_hkUHRMry4JtQuQbNijYZ1a/view?usp=drive_link
