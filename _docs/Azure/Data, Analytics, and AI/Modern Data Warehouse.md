---
layout: page
title: Azure Synapse Analytics
description: Resources for Azure Synapse Analytics
updated: 2022-06-30
permalink: /azure/data-analytics-ai/azure-synapse-analytics
redirect_from:
- /azure/data-analytics-ai/modern-data-warehouse
tags: 
- azure
- data, analytics, and ai
- learning plan
- synapse
- sql server
- data warehouse
---

# Azure Synapse Analytics Readiness Resources

Azure Synapse Analytics is an analytical service evolved from Azure SQL Data Warehouse that brings together enterprise data warehousing and big data analytics. Provisioned or on-demand, Azure Synapse offers a unified experience to ingest, prepare, manage, and serve data for analytics, BI, and machine learning needs.

Content is broken down as follows:

* Keeping Up: latest information and links 
* Fundamentals, Associate, Expert, Specialist: content categorized in increasing level of complexity
* Certifications: relevant Microsoft exams or certifications
* Community resources: user groups, events, blogs

## Keeping Up

The latest updates on Azure Sypanse Analytics.

Azure Synapse Analytics is now generally available as of December 2020. 

* [June 2022 Update](https://techcommunity.microsoft.com/t5/azure-synapse-analytics-blog/azure-synapse-analytics-june-update-2022/ba-p/3535086)
  * Azure Orbital analytics
  * Azure Synapse Success by Design
  * Synapse Data Explorer updates
* [May 2022 Update](https://techcommunity.microsoft.com/t5/azure-synapse-analytics-blog/azure-synapse-analytics-may-update-2022/ba-p/3430970)
  * Data warehouse migration guide for dedicated SQL Pools
  * Apache Spark for Synapse
  * Synapse Data Explorer
  * Data Integration
  * Synapse Link
* [January 2022 Update](https://techcommunity.microsoft.com/t5/azure-synapse-analytics-blog/azure-synapse-analytics-january-update-2022/ba-p/3071681)
  * Additional database templates (Automotive, Genomics, Manufacturing, Pharmaceuticals)
  * SynapseML improvements
  * Data flow connector for Dynamics

## Fundamentals

* [Introducing Azure Synapse Analytics](https://azure.microsoft.com/en-us/resources/videos/ignite-2019-new-introducing-azure-synapse-analytics-the-next-evolution-of-sql-data-warehouse-for-every-data-professional/) (Ignite session / 1 hour)
  * Customer talk track on the problems that Azure Synapse is designed to address.
* [Data Warehouse workloads](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/big-data) (Microsoft Docs)
  * Defines the building blocks and workloads for a Modern Data Warehouse.
  * Big Data is a synonym for Modern Data Warehouse in this article
* [Azure Data Architecture Guide](https://docs.microsoft.com/en-us/azure/architecture/data-guide/) (Microsoft Docs)
  * Azure Data architecture guide is a deep dive into each workload in a Modern Data Warehouse
  * Review all content under the "Guides" directory on the left-hand menu
* [Data Management Patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns/category/data-management) (Microsoft Docs)
  * These are different design patterns your Data Warehouse might need to address
  * Database Developers or Administrator might use these terms to define their current architecture
* [What is Data Engineering?](https://medium.com/datadriveninvestor/what-is-data-engineering-explaining-the-data-pipeline-data-warehouse-and-data-engineer-role-1a4b182e0d16) (3rd Party, Document)
  * Industry definition of a data warehouse, ETL and data engineer
  * Provide a common set of concept and terms you need to know when talking with your customers
* [Understanding Star Schema](https://docs.microsoft.com/en-us/power-bi/guidance/star-schema) (Microsoft Docs)
  * How best to model your business data for analytics
  * Star schemas are defined as dimensional models and central to data warehouse analysis
* [AWS to Azure Services Comparison](https://docs.microsoft.com/en-us/azure/architecture/aws-professional/services
) (Microsoft Docs)
  * Reference guide for alternative Cloud platforms
* [Azure Partner Tech Talks - Modern Data Warehouse](https://aka.ms/azurepartnerstechtalks) (Webinar)
  * Specifically, the Modern Data Warehouse presentation from April 23, 2020
* [Beginner's Guide to Azure Data Factory](https://www.cathrinewilhelmsen.net/series/beginners-guide-azure-data-factory/) (3rd Party)
  * Series of 26 blog posts reviewing the fundamentals of Azure Data Factory
* [Customer References and Use Cases (PPTX)](https://www.microsoft.com/azure/partners/resources/azure-synapse-analytics-customer-references)

## Associate

* [Introducing the Modern Data Warehouse Solution Pattern](https://youtube.com/watch?v=7MDCWgxPnVY) (YouTube, ~20 minutes)
* [Big Data Architectures](https://docs.microsoft.com/en-us/azure/architecture/data-guide/big-data/) (Microsoft Docs)
  * Review all content under "Big Data" directory on left-hand menu
* [Modern Data Warehouse Architecture](https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/modern-data-warehouse) (Microsoft Docs)
  * Reference architecture for a Modern Data Warehouse
* [Implement a Data Warehouse with Azure Synapse Analytics](https://docs.microsoft.com/en-us/learn/paths/implement-sql-data-warehouse/) (Microsoft Docs)
  * Hands-on lab with three modules to complete.
* [Azure SQL Database vs SQL Data Warehouse](https://www.jamesserra.com/archive/2016/08/azure-sql-database-vs-sql-data-warehouse/) (Microsoft Blog)
  * Decision criteria for best Azure Data Service for data warehousing
* [Dimensional Modelling Case Study: eWallet](https://towardsdatascience.com/data-warehouse-dimensional-modelling-use-case-study-ewallet-d9d16f559181) (3rd Party, Document)
* [Power BI Guidance](https://docs.microsoft.com/en-us/power-bi/guidance/) (Microsoft Docs)
  * Review all content in the Data Modeling section.
* [Criteria for Choosing a Data Store](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/data-store-comparison) (Microsoft Docs)
  * Alternative options to relational databases.
* [Azure Data Factory: Mapping Data Flows](https://github.com/kromerm/adfdataflowdocs/blob/master/patterns/adfdataflowlinks.md) (Tutorials)
  * Review all content and complete NYC Taxi Demo Lab
* [Extending on-premises data solutions to the cloud](https://docs.microsoft.com/en-us/azure/architecture/data-guide/scenarios/hybrid-on-premises-and-cloud) (Microsoft Docs)
  * Azure Services required for a Hybrid architecture
* [Securing Data Solutions](https://docs.microsoft.com/en-us/azure/architecture/data-guide/scenarios/securing-data-solutions) (Microsoft Docs)
  * General security requirements needed for any data platform architecture
* [Architect Migration and BCDR](https://docs.microsoft.com/en-us/learn/paths/architect-migration-bcdr/) (Microsoft Docs)

__The following documents are intended to be consumed in order, as they begin with a reference architecture through solution building:__

* [1. Reference Architecture: Automated Enterprise BI with Synapse](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/data/enterprise-bi-adf) (Microsoft Docs)
* [2. Example Workloads: Data warehousing and analytics](https://docs.microsoft.com/en-us/azure/architecture/example-scenario/data/data-warehouse) (Microsoft Docs)
* [3. Solution Ideas: Streaming using HDInsight](https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/streaming-using-hdinsight) (Microsoft Docs)

__Pluralsight Courses:__

* [Implementing a Cloud Data Warehouse in Microsoft Azure Synapse Analytics](https://www.pluralsight.com/courses/microsoft-azure-implementing-cloud-data-warehouses) (3rd Party, $)
* [Modern Data Warehousing at Scale Using Azure Data Factory](https://www.pluralsight.com/courses/big-data-ldn-session-25) (3rd Party)
  * This is a session from Big Data LDN in Nov 2019. This is a good primer/use case on Azure Data Factory for ETL.

## Expert

* [Tutorial: Load data using Azure portal and SSMS](https://docs.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/load-data-wideworldimportersdw) (Microsoft Docs)
* [Tutorial: Load the NY Taxicab Dataset](https://docs.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/load-data-from-azure-blob-storage-using-polybase) (Hands on lab)
* [Building OSS Analytical Solutions with Azure HDInsight](https://docs.microsoft.com/en-us/learn/paths/build-oss-analytical-solutions-az-hdinsight/) (Microsoft Docs)
* [Azure End2End - Azure Data Platform Workshop](https://github.com/fabragaMS/ADPE2E) (Hands on lab)
* [Azure Data Factory - Labs](https://github.com/kromerm/ADF_Labs) (Hands on lab)
* [Azure Synapse Analytics Deep Dive: Perform data engineering and exploration](https://note.microsoft.com/US-NOGEP-WBNR-FY21-02Feb-22-AzureSynapseAnalyticsDeepDivePerformdataengineeringandexploration-SRDEM55626-01_Registration.html) (Webinar)
* [Azure Synapse Analytics Deep Dive: Build automated data integration pipelines with Azure Synapse Pipelines](https://note.microsoft.com/US-NOGEP-WBNR-FY21-02Feb-23-AzureSynapseAnalyticsDeepDiveBuildautomateddataintegrationpipelineswithAzureSynapsePipelines-SRDEM55626-02_Registration.html) (Webinar)
* [Azure Synapse Analytics Deep Dive: Run interactive queries using serverless SQL pool with Azure Synapse Analytics](https://note.microsoft.com/US-NOGEP-WBNR-FY21-02Feb-24-AzureSynapseAnalyticsDeepDiveRuninteractivequeriesusingserverlessSQLpoolwithAzureSynapseAnalytics-SRDEM55626_Registration.html) (Webinar)
* [Azure Synapse Analytics Deep Dive: Optimize a data warehouse with dedicated SQL pools](https://note.microsoft.com/US-NOGEP-WBNR-FY21-02Feb-25-AzureSynapseAnalyticsDeepDiveOptimizeadatawarehousewithdedicatedSQLpools-SRDEM55626_Registration.html) (Webinar)
* [Azure Synapse Analytics Deep Dive: Machine Learning in Azure Synapse Analytics](https://note.microsoft.com/US-NOGEP-WBNR-FY21-02Feb-26-AzureSynapseAnalyticsDeepDiveMachineLearninginAzureSynapseAnalytics-SRDEM55626_Registration.html) (Webinar)

__WhatTheHack events are often in-person in a hands on format.  However, it can be worked on individually and self-paced:__

* [WhatTheHack - Driving Miss Data](https://github.com/microsoft/WhatTheHack/tree/master/003-DrivingMissData) (Hands on lab)
* [WhatTheHack - This Old Data Warehouse](https://github.com/microsoft/WhatTheHack/tree/master/019-ThisOldDataWarehouse) (Hands on lab)

__Microsoft OpenHack events are immersive, multi-day hands on experiences; specifically, the Modern Data Warehouse dives into Azure Synapse, Databricks, Azure Data Factory, and Azure Data Lake.__

* [OpenHack - Modern Data Warehouse](https://openhack.microsoft.com/) (Hands on lab / workshop)
* [CICD For SQL Analytics using SSDT](https://cloudblogs.microsoft.com/sqlserver/2019/11/07/new-in-azure-synapse-analytics-cicd-for-sql-analytics-using-sql-server-data-tools/) (SQL Server Blog)

## Specialist

* [Open Hack Registration Site](https://openhacks.azurewebsites.net/labs/player/openhack_-_modern_data_warehousing_2bd410cacc6b_3_0)
  * Register for a Modern Data Warehouse OpenHack. OpenHacks are a challenge-based lab format; the Modern Data Warehousing OpenHack provides a lab environment with preconfigured resources.
* [Analytics in a Day](https://github.com/abrahams1/azsynapselabsny)
  * Self-guided labs for Analytics in Day workshop.

## Certifications

Exams such as the [70-767 Implementing a Data Warehouse](https://www.microsoft.com/en-us/learning/exam-70-767.aspx) is no longer available and was retired on January 31, 2021. We recommend the new role-based certifications, as these better align to industry trends and the mix of technical skills needed to successfully design and implement Data & AI solutions.

The first two role-based exams, DP-200 and DP-201 have also been retired and replaced with [DP-203 Data Engineering on Microsoft Azure](https://docs.microsoft.com/en-us/learn/certifications/exams/dp-203). DP-203 consolidates all of the goals of DP-200 and DP-201, and includes the latest features in Azure Synapse. 

Passing [DP-203](https://docs.microsoft.com/en-us/learn/certifications/exams/dp-203) is required for the [Microsoft Certified: Azure Data Engineer Associate](https://docs.microsoft.com/en-us/learn/certifications/azure-data-engineer?wt.mc_id=learningredirect_certs-web-wwl) certification.

## Community

* [Azure Synapse Analytics Blog](https://techcommunity.microsoft.com/t5/azure-synapse-analytics-blog/bg-p/AzureSynapseAnalyticsBlog)
* [Power BI User Group](https://www.pbiusergroup.com/home)
* [SQL PASS](https://www.pass.org/)
* [Pragmatic Works: Blog on SQL Server](https://blog.pragmaticworks.com)
* [Blue Granite Blog](https://www.blue-granite.com/blog)
* [Buck Woody's Blog](https://buckwoody.wordpress.com/)
* [James Serra's Blog](https://www.jamesserra.com/)
* [Azure Synapse Tech Community](https://techcommunity.microsoft.com/t5/azure-synapse-analytics/bg-p/AzureSynapseAnalyticsBlog)
