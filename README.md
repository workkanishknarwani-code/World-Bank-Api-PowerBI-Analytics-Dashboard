Project Overview

This project implements an end-to-end data analytics pipeline that extracts global development indicators from the World Bank REST API, processes and structures the data using Python, and builds an interactive Power BI dashboard for multi-country comparative analysis.

The dashboard analyzes economic growth, digital adoption, environmental sustainability, labour market indicators, and health metrics across global regions.

Tech Stack

Python

Pandas

NumPy

Requests

World Bank REST API

Power BI

DAX

Relational Data Modeling

Data Pipeline Architecture
1. API Data Extraction

Connected to World Bank REST API endpoints.

Retrieved country metadata.

Extracted grouped indicators across domains:

Economic Activity & Growth

Labour Market Indicators

Poverty & Inequality

Environmental Indicators

Health Indicators

Technology Indicators

Implemented pagination handling for multi-page API responses.

Added request delay handling to prevent API rate limiting.

2. Data Cleaning and Transformation

Normalized nested JSON responses into structured tabular format.

Extracted key fields:

country_id

country_value

indicator_id

indicator_name

year

value

Filtered dataset for recent observations (post-2015).

Merged indicator datasets with country metadata.

Generated domain-specific structured datasets for BI ingestion.

3. Power BI Data Modeling

Built relational schema:

Fact tables (economic, labour, health, environment, technology)

Country dimension table

Created DAX measures for:

GDP per Capita

GDP Growth

Internet Users (%)

Implemented dynamic filtering by region and year.

Applied clean dashboard design principles with dark theme styling.

Dashboard Features
KPI Metrics

Average GDP per Capita

GDP Growth (%)

Health Expenditure (% of GDP)

Comparative Analysis

Regional comparison of development indicators

Multi-indicator trend analysis by year

Correlation Analysis

Scatter plot: Internet Users vs GDP per Capita

Linear regression trend line

Geographic Visualization

World map showing country-level development metrics

Multi-metric tooltips

Interactive Controls

Region filter

Year filter

Key Insights

Strong positive correlation between digital adoption and economic prosperity.

Regional clustering patterns in economic and technological indicators.

Noticeable variation in growth momentum across income levels.

Structural disparities observed in environmental and development metrics.

Repository Structure
world-bank-api-powerbi-analytics-dashboard/
│
├── World_Bank_Dashboard.pbix
├── project3.py
├── data/
├── images/
│   └── dashboard_preview.png
└── README.md
How to Run
Python Data Pipeline

Install dependencies:

pip install pandas numpy requests

Run the script:

python project3.py
Power BI Dashboard

Open the .pbix file

Refresh data connections

Interact using region and year filters

Project Highlights

Built a scalable API-driven data ingestion workflow

Applied structured data modeling principles

Designed an interactive analytics dashboard

Implemented DAX-based analytical measures

Integrated multi-domain global development indicators
