🇺🇸 Americans Abroad Power BI Dashboard
Year‑Over‑Year Analysis (2022 → 2023)
This project is an interactive Power BI dashboard analyzing how the population of Americans living abroad changed between 2022 and 2023. The analysis uses two independent data sources — FVAP (2022) and AARO/Pinto (2023) — and combines them into a unified, insight‑driven visual experience.

The dashboard highlights migration patterns, country‑level growth and decline, and broader global trends using a clean dimensional model, DAX‑driven calculations, and custom visual indicators.

📊 Key Insights
Mexico shows the strongest year‑over‑year growth (+119%).

Israel also experienced significant expansion (+77%).

Canada grew modestly (+16%).

France saw the sharpest decline (–39%).

United Kingdom declined slightly (–5%).

Across the five comparable countries, the total population increased by 38%.

### 2022 Population — Top 5 Countries (FVAP 2022)
- **Canada:** 909,709  
- **Mexico:** 539,450  
- **United Kingdom:** 343,325  
- **France:** 191,930  
- **Israel:** 159,134  

### Americans Abroad in 2023 — Comparable Countries Only
These values reflect the five countries for which both 2022 (FVAP) and 2023 (AARO/Pinto) data are available, ensuring a consistent year‑over‑year comparison.

- **Mexico:** 1,182,346  
- **Canada:** 1,050,898  
- **United Kingdom:** 325,321  
- **Israel:** 281,137  
- **France:** 117,462  

### Year‑Over‑Year Comparison (2022 → 2023)
- Total comparable population increased by **38%**  
- **Mexico** and **Israel** show the strongest growth  
- **France** shows the largest decline  
- Canada grew modestly, while the United Kingdom declined slightly  

These five countries form the basis of the dashboard’s YoY analysis, ensuring methodological consistency across both datasets.

🧩 Data Sources
FVAP (Federal Voting Assistance Program), 2022  
Population estimates of U.S. citizens living abroad

AARO / Pinto, 2023  
Updated estimates of Americans abroad by country

These datasets differ in methodology, so the dashboard focuses on directional trends rather than strict numerical equivalence.

🏗️ Data Model
The model integrates multiple fact tables (2022 and 2023 population data) connected through shared dimensions.
Year‑over‑year metrics are calculated using DAX rather than a physical YoY table.

Model Components
Fact Tables

FVAP_2022

AARO_2023

Dimension Tables

Dim_Country

Dim_Year

(Optional) Dim_Source

Star Schema (Conceptual)
Code
                 Dim_Country
                       |
                       |
Dim_Year ---- Fact Tables (2022 & 2023)
The YoY comparison is constructed through DAX measures and visuals rather than a physical table.

🧮 DAX Highlights
The dashboard uses DAX to calculate:

Year‑over‑year population change

Percent growth/decline

Conditional formatting indicators

Dynamic titles and tooltips

Example measure (simplified):

DAX
Percent Growth =
DIVIDE(
    [Americans 2023] - [US Citizens 2022],
    [US Citizens 2022]
)
🖼️ Dashboard Features
Horizontal bar charts for 2022 and 2023

Year‑over‑year comparison table

Highlighted growth/decline indicators

Global map visualization

Clean, accessible layout

Insight‑driven design choices

📁 Repository Structure
Code
/screenshots        → Dashboard images (add yours here)
/data               → (Optional) Source files or documentation
Americans-Abroad-PowerBI-Dashboard.pbix
README.md
🧠 Skills Demonstrated
Power BI (Modeling, DAX, Visualization)

Data cleaning and transformation

Multi‑source data integration

Dimensional modeling

Insight communication

Visual storytelling

Portfolio‑ready documentation

📥 How to Use
Download the .pbix file from this repository

Open in Power BI Desktop

Explore the visuals, filters, and YoY analysis

📌 Future Enhancements
Add additional countries as data becomes available

Expand to multi‑year trend analysis

Add drill‑through pages

Incorporate demographic segmentation (if data allows)
