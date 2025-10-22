# Supply-Chain-Optimization-using-Azure-Data-Engineering

Overview
This project demonstrates an end-to-end Azure Data Engineering pipeline designed to optimize supply chain operations by improving data visibility, security, and efficiency across multiple stages from ingestion to reporting.
________________________________________
Utilized Medallion Architecture to integrate ADF, Databricks, Synapse, and Power BI.
Each layer is governed, monitored, and secured with Microsoft Entra ID and role-based access control (RBAC).
________________________________________
Tech Stack
    Ingestion	- Azure Data Factory
    Storage	- Azure Data Lake Gen2
    Processing - Azure Databricks (PySpark)
    Modeling - Azure Synapse Analytics
    Visualization	- Power BI
__________________________
Pipeline Flow:
1.	Data Ingestion (Bronze Layer)
- Created dynamic pipelines in Azure Data Factory to pull raw data from the source.
- Stored data in Azure Data Lake Gen2 under the Bronze container.

2.	Data Transformation (Silver Layer)
  
- Connected Azure Databricks to the Data Lake.
- Performed data cleaning, transformations, and aggregations using PySpark.
- Wrote processed data to the Silver container (Silver Layer).

3.	Data Modeling & Storage (Gold Layer)
- Created Synapse Analytics workspace.
- Built external tables, schemas, and views to organize curated data.
- Data stored in the Gold container for analytics.

4.	Visualization & Insights
- Integrated Power BI with Synapse for real-time reporting.
- Designed KPIs and visuals
________________________________________
Business Impact

This pipeline enhances data transparency, reduces latency, and ensures secure, automated reporting for supply chain decisions, minimizing manual data handling and improving efficiency.
________________________________________
