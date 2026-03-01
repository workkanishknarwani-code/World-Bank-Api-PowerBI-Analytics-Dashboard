![Dashboard Preview](dashboard_preview.png)

## Project Overview

- Built an end-to-end data pipeline using the World Bank REST API  
- Processed global development indicators using Python  
- Designed an interactive Power BI dashboard for multi-country comparative analysis  
- Analyzed economic growth, digital adoption, environmental sustainability, labour, and health indicators  

---

## Tech Stack

- Python  
- Pandas  
- NumPy  
- Requests  
- World Bank REST API  
- Power BI  
- DAX  
- Relational Data Modeling  

---

## Data Pipeline Architecture

### 1. API Data Extraction

- Connected to World Bank REST API endpoints  
- Retrieved country metadata  
- Extracted grouped indicators across domains:
  - Economic Activity & Growth  
  - Labour Market Indicators  
  - Poverty & Inequality  
  - Environmental Indicators  
  - Health Indicators  
  - Technology Indicators  
- Implemented pagination handling for multi-page API responses  
- Applied request throttling to avoid API rate limits  

---

### 2. Data Cleaning and Transformation

- Normalized nested JSON API responses into tabular structure  
- Extracted structured fields:
  - `country_id`  
  - `country_value`  
  - `indicator_id`  
  - `indicator_name`  
  - `year`  
  - `value`  
- Filtered dataset for recent observations (post-2015)  
- Handled missing and null values  
- Merged indicator datasets with country metadata  
- Created domain-specific structured datasets for BI ingestion  

---

### 3. Data Modeling in Power BI

- Built relational schema:
  - Fact tables (economic, labour, health, environment, technology)  
  - Country dimension table  
- Established relationships between fact and dimension tables  
- Ensured consistent country-level joins across datasets  
- Implemented aggregation logic for regional analysis  

---

### 4. DAX Measures Implementation

- Created GDP per Capita measure  
- Created GDP Growth measure  
- Created Internet Users (%) measure  
- Built average and regional aggregation calculations  
- Applied context-aware filtering for dynamic visuals  

---

## Dashboard Features

### 1. KPI Cards

- Average GDP per Capita  
- GDP Growth (%)  
- Health Expenditure (% of GDP)  

---

### 2. Comparative Regional Analysis

- Regional comparison of health expenditure  
- Multi-indicator trend analysis by year  
- Dynamic filtering using region slicer  

---

### 3. Correlation Analysis

- Scatter plot: Internet Users vs GDP per Capita  
- Linear regression trend line  
- Country-level distribution visualization  

---

### 4. Geographic Visualization

- Country-level world map  
- Interactive tooltips displaying multiple development metrics  
- Region-based filtering  

---

## Key Insights

- Positive correlation between internet penetration and GDP per Capita  
- Regional clustering patterns in development metrics  
- Variation in economic growth momentum across income groups  
- Structural disparities observed in technological and environmental indicators  

---

## Repository Structure


world-bank-api-powerbi-analytics-dashboard/
│
├── World_Bank_Dashboard.pbix
├── project3.py
├── data/
├── images/
│ └── dashboard_preview.png
└── README.md


---

## How to Run

### Python Data Pipeline

1. Install dependencies:

pip install pandas numpy requests

2. Run the script:

python project3.py


---

### Power BI Dashboard

1. Open the `.pbix` file  
2. Refresh data connections  
3. Interact using region and year filters  

---

## Project Highlights

- Built a scalable API-driven data ingestion workflow  
- Applied structured relational data modeling principles  
- Designed an interactive analytics dashboard in Power BI  
- Implemented DAX-based analytical measures  
- Integrated multi-domain global development indicators
- Designed an interactive analytics dashboard in Power BI
- Implemented DAX-based analytical measures
- Integrated multi-domain global development indicators
