# 🚀 Data Warehouse and Analytics Project

Welcome to the **Data Warehouse and Analytics Project** repository! 🚀

This project demonstrates a comprehensive data warehousing and analytics solution, from building a data warehouse to generating actionable insights.

Designed as a portfolio project, it highlights industry best practices in **data engineering, ETL, data modeling, SQL development, and analytics**.

---

## 🏗️ Data Architecture

The data architecture for this project follows the **Medallion Architecture**, consisting of three layers:

### 🥉 Bronze Layer

Stores raw data as-is from the source systems.

- Data is ingested from CSV files
- Raw ERP data
- Raw CRM data
- No major transformations are applied

### 🥈 Silver Layer

Contains cleaned and standardized data prepared for analytical use.

- Data cleansing
- Data validation
- Standardization
- Data normalization
- Resolving data quality issues
- Applying transformation rules

### 🥇 Gold Layer

Contains business-ready data modeled for reporting and analytics.

- Fact tables
- Dimension tables
- Star schema
- Business-ready data
- Optimized analytical queries

### Architecture Overview

```text
ERP CSV Files ─────┐
                   │
                   ▼
             ┌─────────────┐
             │   Bronze    │
             │  Raw Data   │
             └──────┬──────┘
                    │
                    ▼
             ┌─────────────┐
             │   Silver    │
             │  Cleansing  │
             │Transformation│
             └──────┬──────┘
                    │
                    ▼
             ┌─────────────┐
             │    Gold     │
             │ Star Schema │
             └──────┬──────┘
                    │
                    ▼
             ┌─────────────┐
             │  Analytics  │
             │ & Reporting │
             └─────────────┘
                    ▲
                    │
CRM CSV Files ──────┘
📖 Project Overview

This project focuses on building a modern data warehouse using SQL Server to consolidate sales data from two different source systems: ERP and CRM.

The project covers the complete data pipeline, from raw data ingestion to analytical reporting.

Main Components
🏛️ Data Architecture
🔄 ETL Pipelines
🧩 Data Modeling
🧹 Data Cleaning & Transformation
📊 SQL Analytics
📈 Reporting & Business Insights
🧪 Data Quality Testing
📚 Technical Documentation
🎯 Skills Demonstrated

This repository showcases practical experience in:

Skill	Description
SQL Development	Writing SQL queries for ETL, transformation, and analytics
Data Engineering	Building data pipelines and warehouse layers
Data Architecture	Designing a Medallion Architecture
ETL Development	Extracting, transforming, and loading data
Data Modeling	Developing fact and dimension tables
Data Analytics	Generating business insights using SQL
Data Quality	Identifying and resolving data quality issues
Documentation	Documenting architecture, data models, and processes
🛠️ Tools & Technologies
Tool	Purpose
SQL Server Express	Database and data warehouse
SQL Server Management Studio (SSMS)	Database management and SQL development
SQL	ETL, transformations, and analytics
Git & GitHub	Version control and repository management
Draw.io	Architecture, data flow, and data model diagrams
Notion	Project planning and documentation
🚀 Project Requirements
🏗️ Building the Data Warehouse
🎯 Objective

Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

📌 Specifications
📂 Data Sources

Data is provided by two source systems:

ERP
CRM

The source data is provided as CSV files.

🧹 Data Quality

Data quality issues should be identified and resolved before the data is used for analysis.

This includes:

Handling invalid values
Standardizing inconsistent formats
Handling missing values
Identifying duplicate records
Applying appropriate transformations
🔗 Data Integration

ERP and CRM data are integrated into a single, user-friendly data model designed for analytical queries.

📅 Scope

The project focuses on the latest available dataset only.

Historical data tracking and historization are not required.

📚 Documentation

Clear documentation is provided for:

Data architecture
Data flow
ETL processes
Data models
Data catalog
Naming conventions

The documentation is designed to support both business stakeholders and analytics teams.

📊 BI & Analytics
🎯 Objective

Develop SQL-based analytics to deliver detailed insights into key business areas.

👥 Customer Behavior

Analyze customer purchasing behavior and sales activity.

Examples include:

Customer sales contribution
Purchase frequency
Top customers
Customer-level sales trends
📦 Product Performance

Analyze product-level sales performance.

Examples include:

Top-selling products
Product revenue contribution
Product sales trends
Product category performance
📈 Sales Trends

Analyze sales performance over time.

Examples include:

Monthly sales trends
Yearly sales performance
Revenue trends
Order trends
Quantity trends
📂 Repository Structure
data-warehouse-project/
│
├── datasets/                           
│   └── Raw ERP and CRM datasets
│
├── docs/                               
│   ├── etl.drawio                      
│   ├── data_architecture.drawio        
│   ├── data_catalog.md                 
│   ├── data_flow.drawio                
│   ├── data_models.drawio              
│   └── naming-conventions.md           
│
├── scripts/                            
│   ├── bronze/                         
│   │   └── Raw data extraction and loading
│   │
│   ├── silver/                         
│   │   └── Data cleaning and transformation
│   │
│   └── gold/                           
│       └── Analytical models and star schema
│
├── tests/                              
│   └── Data quality and validation tests
│
├── README.md                           
├── LICENSE                             
├── .gitignore                          
└── requirements.txt                    
🔄 ETL Process

The ETL process follows a layered approach:

              ┌───────────────┐
              │  ERP CSV Data │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │    Bronze     │
              │   Raw Data    │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │    Silver     │
              │ Clean &       │
              │ Transform     │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │     Gold      │
              │ Star Schema   │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │   Analytics   │
              │ & Reporting   │
              └───────────────┘
                      ▲
                      │
              ┌───────┴───────┐
              │  CRM CSV Data │
              └───────────────┘
⭐ Data Modeling

The Gold layer is modeled using a Star Schema optimized for analytical workloads.

                  ┌─────────────────┐
                  │  Dim Customers  │
                  └────────┬────────┘
                           │
                           │
┌─────────────────┐        ▼        ┌─────────────────┐
│  Dim Products   │──── Fact Sales ────│    Dim Date    │
└─────────────────┘        │        └─────────────────┘
                           │
                           │
                  ┌────────▼────────┐
                  │ Dim Categories  │
                  └─────────────────┘

The model separates:

Fact tables → measurable business events
Dimension tables → descriptive business attributes

This structure simplifies analytical queries and reporting.

🧪 Data Quality & Testing

The project includes a dedicated tests/ directory for data validation and quality assurance.

Testing includes:

Duplicate record checks
NULL value checks
Data type validation
Date validation
Referential integrity
Data consistency
Transformation validation
Source-to-target reconciliation
📚 Documentation

Detailed project documentation is available in the docs directory.

File	Description
etl.drawio	ETL techniques and methods
data_architecture.drawio	Data warehouse architecture
data_catalog.md	Dataset and field descriptions
data_flow.drawio	Data flow diagram
data_models.drawio	Star schema and data models
naming-conventions.md	Naming guidelines for tables and columns
📈 Analytics

The Gold layer is used to generate business-oriented SQL reports covering:

👥 Customer Analysis
📦 Product Analysis
📈 Sales Analysis
📅 Time-Based Trends
💰 Revenue Analysis
🏆 Top Customers and Products
📊 Key Business Metrics

The goal is to transform raw operational data into structured information that supports business analysis and decision-making.

🗺️ Project Roadmap
 Project requirements defined
 Repository structure created
 Data architecture designed
 Bronze layer implementation
 Silver layer implementation
 Gold layer implementation
 Data quality tests
 Analytical SQL queries
 Documentation
 Final analytics and reporting
📸 Project Documentation

Architecture diagrams, ETL processes, data flows, and data models are available in the docs directory.

📬 Connect
Project Author

Bekir Enes Şiranlı

💻 GitHub: github.com/enessiranli

Feel free to explore the repository, provide feedback, or connect with me.

🛡️ License

This project is licensed under the MIT License.

You are free to use, modify, and share this project with proper attribution.

⭐ If you find this project useful, feel free to star the repository!
