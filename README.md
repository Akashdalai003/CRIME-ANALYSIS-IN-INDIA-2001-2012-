📈CRIME ANALYSIS DASHBOARD (2001–2012)

This project analyzes a comprehensive Indian crime dataset spanning 
from *2001 to 2012, containing **multiple States, **hundreds of Districts, and **various Crime Types* reported each year. 
The goal of this dashboard is to give an interactive, accurate, and advanced analytical view of crime trends across India.
A complete semantic data model was built to support clean filtering, advanced KPIs, drilldowns, and performance-optimized reporting.

![image alt](https://github.com/Akashdalai003/CRIME-ANALYSIS-DASHBOARD/blob/21e0b7fabcad8bbe64a5b54d62d16dd42d1bc08d/Screenshot%202025-11-30%20130531.png)
🧹 *DATA CLEANING & TRANSFORMATION:*

The original dataset required extensive cleaning to ensure accurate analytics.

 [*KEY CLEANING STEPS PERFORMED:*]

* *Removed 'Total' rows* from the District, State, and Crime Type columns (e.g., “Total”, “Total IPC Crimes”) to avoid inflated values.
* *Converted all crime count columns* from text to numeric data types.
* *Unpivoted the dataset* (where required) to convert wide crime columns into a structured Fact table.
* *Eliminated duplicate entries* caused by State/District total summaries.
* *Separated categorical columns* into dedicated dimension tables.
* *Created surrogate keys* for State_ID and District_ID.
* *Ensured consistent relationships* between Fact and Dimension tables.

---

## 🧱 DATA MODEL DESIGN

A star-schema model was implemented for clean filtering and high performance.
 *Tables Used in the Data Model:*

#### *1. Fact_Crimes (Fact Table)*

Contains all numerical and relationship-driving data.

##### Columns:

* Crime_ID (Index/Surrogate Key)
* District_ID
* Year_ID
* Crime_Type
* Crime_Count (numeric)

#### *2. Dim_State*

Contains unique list of states.

##### Columns:

* State_ID
* State_Name
* Region (manually added based on geography)

#### *3. Dim_District*

Contains the cleaned list of districts.

##### Columns:

* District_ID
* District_Name
* State_ID (relationship to Dim_State)

#### *4. Dim_Region*

Contains the no.of Region

##### Columns:

* REGION_ID
* REGION
* STATE/UT

#### *5. Dim_Year*

Calendar year table.

##### Columns:

* Year

---

## 📊 VISUALS INCLUDED IN THE DASHBOARD

A dark-theme, modern, interactive dashboard was created.

### *KPI CARDS:*

* Total States
* Total Districts
* Total Crime Types
* Total Crimes
* Top State      (Name + Total Crimes)  [MULTI ROW CARD]
* Top District   (Name + Total Crimes)  [MULTI ROW CARD]
* Top Crime Type (Name + Total Crimes)  [MULTI ROW CARD]
* YOY CRIME % (shows in % how the no. of crime has been changed compared to the previous year)
* YOY Crime Change
  
### *MAIN VISUALS:*

* *Total Crime by State* (Line & Clustured Column Chart)
* *Total Crime by District* (Clustured Bar Chart )
* *Total Crime by Type* (Clustured Bar Chart)
* *Crime Trend Over Years* (Line Chart)
* *Crime Distribution by Region* (Map – Azure Map)
  
### *Filters/Slicers Added:*

* Year
* State
* District
* Region
* Crime Type

---

## 🧠 Key DAX Measures (Examples)

* Total Crimes
* Top State Name with Crime Count
* Top District Name with Crime count 
* Top Crime Type
* YoY Crime Change
* YoY % Change [
* Total State
* Total District
* Total Crime

---

## 🚀 Project Purpose

To build a real‑time, interactive, and professional‑grade Power BI dashboard using:

* Clean data engineering
* Proper semantic modeling
* Advanced KPIs & DAX
* Modern visual storytelling

This dashboard can help governments, researchers, policymakers, and analysts identify crime trends and take meaningful action.

---

## 📌 Future Improvements

* Add forecasting using Time Intelligence
* Add clustering of high‑crime districts
* Integrate ML predictions 
* Create bookmark‑based navigation pages
