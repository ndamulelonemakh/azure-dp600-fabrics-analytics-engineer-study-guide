# My Experience & Tips for Taking Azure DP 600 - Fabric Analytics Engineer Associate Exam

- **Created:** February 17, 2024 1:41 AM
- **Author:**  [Ndamulelo Nemakhavhani](https://www.linkedin.com/in/ndamulelonemakhavhani/)


In this guide, I will share my experience of taking the [Microsoft DP-600 beta exam](https://learn.microsoft.com/en-us/credentials/certifications/exams/dp-600/) and provide some useful tips to help you prepare for it. Before we proceed further, I would like to explain why I believe this exam is worth taking for any *Data* or *Engineering* professional looking to stay ahead of the competition.

1. **Data Analysts** - In my opinion, this exam(actually [Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/get-started/microsoft-fabric-overview) in general) is ideally designed to empower data analysts to manage the entire data lifecycle with less reliance on Data Engineers and/or Machine Learning Engineers. If you identify with this role, I strongly recommend that you take this exam to advance your career to the next level.
2. **Data Engineers** - If you are currently a Data Engineer who prefers not to spend too much time setting up infrastructure, or if you need a platform to quickly test some ETL or ELT solutions, you should look at [Microsoft Fabric](https://www.microsoft.com/en-us/microsoft-fabric).
3. **Data Scientists** - Often, data scientists spend more time managing data and addressing data quality issues than actually building models with good explainability and high accuracy. Microsoft Fabric, with its serverless data processing options, can expedite the time to inference for data scientists.
4. **Engineers** - Lastly, If you are an Engineer looking to specialize in a data role, Microsoft Fabric offers arguably the quickest way to learn the end-to-end big data analytics lifecycle without having to master too many tools.

> **Disclaimer: P**lease note that this is not an exhaustive list of topics. Furthermore, I have a solid background in Engineering and Machine Learning, so some of my views might be biased.
> 

# What problem does Microsoft Fabric solve?

- If you’re like me, the more you explore Microsoft’s offerings, you might find yourself asking, “Don’t we already have [Azure Synapse Analytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/) for this?”
- While Synapse Analytics does offer similar capabilities, it requires more setup and administration compared to Fabric.
- This means that you can potentially do enterprise-scale analytics on Fabric even if your technical/coding skills are limited.
- Fabric is natively serverless with intuitive drag-and-drop workflows. This eliminates issues such as skill shortages and may reduce time to market.
- However, it is worth noting that the lack of flexibility might pose challenges when troubleshooting errors.
- I found it helpful to view Fabric as a sort of superset platform that encompasses all Synapse capabilities and more!

# Microsoft Fabric Subscription Options

- Get started with a Free Trial
- Purchase via Power BI premium workspace license
- Purchase pay-as-you-go capacity through the Azure Portal

***NB:** Before you can use fabric, you will need a work or school email address. Personal Outlook accounts are not currently supported.*

# Big Data Solution Design Considerations

1. Where is the data?
2. Which interfaces or protocols will you need to move the data?
3.  How frequently is the data generated?
4. What is the volume?
5. What is the native format of the data?
6. What skills do you have in your team?
7. What is the acceptable latency? i.e. Is this a Batch or streaming solution?
8. and more

# Data Transformation

- Apache Spark Overview
- Data Flow Gen2
- Notebook transformations with PySpark
    - PySpark basics *****
    - PySpark functions *****
        - Filter
        - Select
        - Partition By
        - Write
        - Read
        - Group
    - Different patterns of loading data e.g. load from Blob Storage
    - Writing transformed data to a File
    - Writing transformed data to a Delta Table
- Write optimization
    - V-order *****
    - File-size optimization
- Data Factory pipeline
    - Built-in examples
    - Copy data Activity *****
    - Dataflow Gen2 Integration

# Data Lakehouse

- Schema on reading
- Medallion architecture
- Delta Lake - SQL abstraction over files
- Streaming patterns
- Incremental loads i.e. append vs overwrite
- Big data file formats
    - Parquet
    - Avro
    - Compression
- File partitioning

# Data Warehouse

- SQL Editor
- Visual Editor
- T-SQL essentials
    - Functions
    - Stored procedures
    - Views
    - Extended functions e.g. Machine learning
- Monitoring
    - CU Metrics app
    - DMV
    - Query Insights
    - Special tables for observability
- Fact vs Dimension Tables
- SCD - slowly changing dimensions
    - Type 1
    - Type 2
- Partitioning

# Synapse real-time analytics

- KQL - Kusto Query Language
- Window Functions
- Data Source Types
- Data Destination Types

# Power BI Essentials

I left this section last because I assume the majority of people taking this exam will be experienced Data Analysts with extensive knowledge of Power BI. However, if you are a  **Power BI novice**, I **strongly suggest you spend as much time as possible doing practical examples**. More especially, make sure you are proficient in reading and writing DAX queries.

- Data modelling e.g. Start schema
    - Model relationships
    - Relationship functions
- DAX
    - Syntax
    - Popular Functions
    - DAX Studio
    - Tabular Editor
    - Query Optimization
    - Direct Lake
- Temporal analysis
    - Aggregation functions e.g. DAYSSINCELASTQUATER
- XLMA
- Report performance & scaling considerations
    - Direct Query vs Import
    - Large-scale storage format
- Data refresh

# Deployment patterns for Power BI Reports

- Continuous Integration/ Continuous Delivery
- Continuous Integration/ Continuous Deployment
- Power BI File formats
- Deployment methods
    - Git (Azure DevOps)
    - SharePoint
    - OneDrive
    - Power BI deployment pipeline
- Power BI report naming conventions
- Managing change conflicts
- Power BI deployment rules

# Reusable Power BI Data Assets

- Power BI service share datasets
- Power BI Templates
- Endorsement & certification
- Data Lineage
- Permissions
- Sensitivity classification
- Row-level security
- Column-level security

# Microsoft Fabric Administration and Operations

- Capacity planning i.e. SKU
- Fabric Admin Center
- Licensing
    - Workspace
    - Per user etc.
- Security
    - Workspace permissions
    - Microsoft Entra ID Integration
    - Data sharing options

---

# Closing Thoughts

As you can see, the exam essentially covers the entire lifecycle of an analytics pipeline, catering to organizations of any size. Given the cost considerations, it might be particularly suitable for medium to large enterprises seeking to break down data silos. In closing here are some helpful hacks to prioritize the study materials according to your current job role.

- **Data Engineer -** Review the security and capacity configurations and practice building Power BI reports extensively, especially using DAX and Power Query M.
- **Data Analyst -** Although you can navigate Fabric with no coding experience, proficiency in coding is required for the exam. Understand the basic syntax in Python and work through numerous PySpark examples. Additionally, invest time in understanding how data is sourced and transformed before it is used in Power BI reports. Going through material for data engineering exams such as [Azure DP203](https://learn.microsoft.com/en-us/credentials/certifications/exams/dp-203/) might be beneficial if time permits.
- **Engineers -** Focus on understanding the end-to-end data lifecycle within Fabric. This includes data ingestion, transformation, storage, analysis, and visualization. Hands-on practice with real-world scenarios will likely lead to success compared to reading through learning materials.
- **Data scientists** - This exam will not include any model training questions, hence you will need to upskill in concepts from Data Engineering and Power BI. Real-world practice will likely increase your chances of success compared to reading.

The scope of the exam is quite extensive. Unless you are studying full-time, it is unlikely that you will cover every topic in detail. The most effective strategy that has consistently worked for me involves spending some time on the early chapters of the [Official Microsoft Learn Learning Path](https://learn.microsoft.com/en-us/credentials/certifications/exams/dp-600/), and then transitioning to hands-on exercises as soon as possible. You will realize as you progress that once you understand the basics of the Data Analytics lifecycle, you should be able to answer most questions using common sense. Good luck!

# Links

* [Study guide for Exam DP-600: Implementing Analytics Solutions Using Microsoft Fabric](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/dp-600)

* [Course DP-600T00-A: Microsoft Fabric Analytics Engineer - Training](https://learn.microsoft.com/en-us/training/courses/dp-600t00)

* [Buy a Microsoft Fabric subscription - Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/enterprise/buy-subscription)
