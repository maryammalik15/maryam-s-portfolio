## Ambulance Handover Delays | Operational Intelligence & Strategic Analysis

**NHS England · October 2023 – July 2026**
--- 
# Context & Overview

### Project Overview
An end-to-end operational intelligence project investigating ambulance handover delays across NHS England.
The project uses publicly available NHS operational data to identify geographical disparities, performance trends and areas of operational pressure. It combines Python based data extraction, SQL data engineering, exploratory analysis and Excel visualisation to transform raw datasets into meaningful business insights.
The objective is to demonstrate how data can support operational decision making, performance monitoring and strategic prioritisation using evidence based methods.

### Operational Question
Where are ambulance handover delays most concentrated, what patterns distinguish consistently underperforming areas from isolated extreme cases, and where should operational investigation be prioritised? By identifying patterns and areas for further investigation, we can inform investigation for definitive causes of handover delays.

### Project Information
 
|  Attribute  |  Details |
| --- | --- |
| Project type  | Operational Intelligence / Strategy & Operations  |
| Industry | Healthcare / Public Sector |
| Data coverage | October 2023 – July 2026 |
| Source files | 34 monthly datasets |
| Primary data | NHS England Ambulance Handover Data |
| Database | Google BigQuery |
| Programming | Python (Google Colab) |
| Data extraction | Python Web Scraping |
| Data cleaning | SQL (BigQuery) |
| Data wrangling | Excel / Pivot Tables |
| Analysis | SQL (BigQuery) |
| Visualisation | Microsoft Excel |
| Automation | Python, SQL and Power Query (planned development) |

--- 

# Project Workflow

### Stage 01 — Data Sourcing & Extraction

**Objective:**
- Independently source and consolidate publicly available operational data. Identified NHS England's Ambulance Management Information – Handovers dataset.

- Used Python in Google Colab to automate the extraction of monthly source files. Collected 34 monthly datasets covering October 2023 to July 2026.

- Consolidated the source material into a format suitable for database ingestion, in the form of a CSV file

**Challenges and considerations:** 

- Working with multiple monthly files rather than one consistent dataset, appending produced unwanted and empty lines

- Handling changes in source structures and column availability. Over the years, table formatting changed and new columns like 45 minute delays were introduced.

- Ensuring the correct reporting periods and source files were captured. Made sure appending matched based on column titles and not column order.

**Skills demonstrated:** Python, web scraping, data acquisition, source management and reproducibility.

### Stage 02 — Data Cleaning & Standardisation

**Objective:** Transform inconsistent raw source data into a reliable analytical dataset using Google BigQuery and SQL. I developed the cleaning and standardisation process to prepare the monthly data for analysis.

- Standardising column names and data structures across monthly datasets.

- Addressing inconsistent schemas, missing or blank fields, Duplicated entries.

- Reviewing numerical fields and ensuring consistent data types.

- Standardising reporting periods and geographical identifiers.

- Investigating unknown and unclassified handover records.

- Validating aggregated figures against the original source data.

|  **Key Cleaning Challenges**  |  **Solution** |
| --- | --- |
|The monthly datasets were not consistent across 3 years. Structural differences and missing fields made direct consolidation and comparison unreliable without additional transformation. | Use SQL transformations to create a consistent analytical structure, allowing comparisons across reporting periods and geographical areas. Structure was adopted according to latest reports to future proof consolidation moving forwards |
| False trust matching on ICB names, ICB names were updated in July 2026 | Supplementary datasets from NHS reports on updates were used to match ICB names to trust according to current naming |

**Skills demonstrated:** SQL, BigQuery, data quality, data validation, data transformation and ETL principles.

### Stage 03 — Data Wrangling & Preparation

**Objective:** Structure the cleaned data into meaningful analytical views to test hypotheses and build on with detailed business questions.

Using Excel to manipulate, aggregate and organise the data using Pivot Tables to structure analysis across different levels of granularity:

- Regional performance.

- Individual NHS Trust performance.

- Monthly performance trends.

- Handover duration thresholds.

- Total handovers and associated operational hours.

|  **Key Analytics Challenges**  |  **Solution** |
| --- | --- |
| Identifying the drivers of poor regional performance | Developed a Trust-level analytical approach to distinguish isolated outliers from wider patterns |
| Interpreting nested handover thresholds | Investigated how the 15, 30, 45 and 60-minute measures relate to one another to avoid double counting |
| Comparing different levels of aggregation | Separated regional, Trust and monthly performance measures |
| Understanding cumulative hours versus average duration | Examined volume and duration as separate performance indicators instead of dismissing them as interchangeable KPIs |

**Skills demonstrated:** Excel, Pivot Tables, data aggregation, data structuring and analytical preparation.

### Stage 04 — Exploratory Analysis & SQL Investigation

- Geographical variation: Which regions consistently experience the longest ambulance handover delays?

- Trust-level performance: Are poor regional results driven by a small number of underperforming Trusts or a wider pattern across multiple Trusts?

- Concentration of delays: Are operational hours disproportionately affected by a small number of extreme handovers, or by a larger volume of moderately delayed cases?

- Seasonality: Are there recurring periods of increased handover pressure?

- Severity: How does performance change across the 15, 30, 45 and 60-minute thresholds?

- Operational prioritisation: Which geographical areas warrant further investigation based on their volume, severity and cumulative operational burden?

**Skills demonstrated:** SQL querying, analytical reasoning, hypothesis testing, segmentation, performance benchmarking and problem-solving.

### Stage 05 — Visualisation & Performance Dashboard

**Objective:** Translate analytical outputs into an accessible performance monitoring tool.

I developed an Excel dashboard to present the findings and enable comparisons across regions and NHS Trusts. The dashboard is designed to help stakeholders move from understanding overall performance to identifying where further investigation may be needed. Components include:

- Regional KPI comparison.

- Average handover duration.

- Percentage of handovers exceeding 15, 30, 45 and 60 minutes.

- Total handover hours.

- Monthly performance trends.

- Trust-level performance comparisons.

- Identification of operational outliers.

**Skills demonstrated:** Excel dashboards, KPI development, conditional formatting, data visualisation and data storytelling.

---
