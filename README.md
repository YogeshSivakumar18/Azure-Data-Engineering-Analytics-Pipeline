# Cloud based data engineering & analytics pipeline for a unified solution

## Overview

This project demonstrates an end-to-end Azure Data Engineering pipeline designed to optimize supply chain operations by improving data visibility, security, and efficiency across multiple stages from ingestion to reporting.
________________________________________
Utilized Medallion Architecture to integrate ADF, Databricks, Synapse, and Power BI.
Each layer is governed, monitored, and secured with Microsoft Entra ID and role-based access control (RBAC).

![Architecture Overview](Data%20Architecture.png)
________________________________________
## Tech Stack

    Ingestion	- Azure Data Factory
    Storage	- Azure Data Lake Gen2
    Processing - Azure Databricks (PySpark)
    Modeling - Azure Synapse Analytics
    Visualization	- Power BI
    Identity & Security - Microsoft Entra ID + RBAC + Key Vault
__________________________
## Pipeline Flow:

1.	Data Ingestion (Bronze Layer)
- Created dynamic pipelines in Azure Data Factory to pull raw data from the source.
- Configured linked services and datasets with managed identities via Microsoft Entra ID.
- Stored data in Azure Data Lake Gen2 under the Bronze container.

![Azure Data Factory Pipeline](Azure%20Data%20Factory%20Pipeline.png)

2.	Data Transformation (Silver Layer)
  
- Connected Azure Databricks to the Data Lake using Service Principal authentication (Entra ID).
- Performed data cleaning, transformations, and aggregations using PySpark.
- Wrote processed data to the Silver container (Silver Layer).

[![Databricks Notebook](Icon.svg)](Databricks%20Transformations.ipynb) **Click the Icon to have a look at the notebook**

3.	Data Modeling & Storage (Gold Layer)
- Created Synapse Analytics workspace.
- Built external tables, schemas, and views to organize curated data.
- Applied row-level security (RLS) and RBAC via Entra ID to enforce controlled access.
- Data stored in the Gold container for analytics.

![Synapse Analytics Workspace.png](Synapse%20Analytics%20Workspace.png)

4.	Visualization & Insights
- Integrated Power BI with Synapse for real-time reporting.
- Designed KPIs and visuals

![Power BI Dashboard](BI%20Dashboard%20Screenshot%20.png)
________________________________________
## Business Impact

This pipeline enhances data transparency, reduces latency, and ensures secure, automated reporting for supply chain decisions, minimizing manual data handling and improving efficiency.
________________________________________
