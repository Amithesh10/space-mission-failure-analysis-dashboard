# 🚀 Space Mission Failure Analysis Dashboard

## 📌 Project Overview

The **Space Mission Failure Analysis Dashboard** is an interactive Power BI project designed to analyze mission performance, launch vehicle efficiency, mission outcomes, costs, fuel consumption, payload capacity, and scientific yield across multiple space missions.

The dashboard provides a comprehensive view of mission operations through advanced data modeling, DAX calculations, and interactive visualizations, enabling stakeholders to identify trends, evaluate mission success, and make data-driven decisions.

---

## 🎯 Business Problem

Space missions involve significant investments, resources, and operational risks. Organizations require a centralized analytics solution to:

* Monitor mission success and failure rates
* Evaluate launch vehicle performance
* Analyze mission costs and resource utilization
* Compare mission types and outcomes
* Track scientific yield and mission efficiency
* Identify long-term performance trends

This dashboard transforms raw mission data into actionable insights through interactive reporting.

---

## 📊 Dashboard Pages

### 1. Overview

Provides a high-level summary of mission performance.

**Key Metrics**

* Total Missions
* Successful Missions
* Partial Success Missions
* Average Success Rate
* Average Mission Cost
* Average Duration

**Visuals**

* KPI Cards
* Mission Trend Analysis
* Outcome Distribution
* Vehicle Comparison

---

### 2. Mission Trend Analysis

Analyzes mission performance over time.

**Insights**

* Year-wise Mission Count
* Success Rate Trends
* Cost Trends
* Scientific Yield Trends
* Distance Covered Analysis

---

### 3. Vehicle Analysis

Evaluates launch vehicle performance.

**Insights**

* Vehicle-wise Mission Distribution
* Success Rate by Vehicle
* Payload Capacity Comparison
* Cost Performance Analysis
* Best and Worst Performing Vehicles

---

### 4. Mission Type Analysis

Compares different mission categories.

**Mission Categories**

* Exploration
* Research
* Colonization
* Mining

**Insights**

* Success Rate by Mission Type
* Scientific Yield Comparison
* Average Duration
* Mission Outcome Distribution

---

### 5. Cost & Resource Analysis

Analyzes operational efficiency and resource utilization.

**Insights**

* Cost per Distance
* Fuel Consumption Analysis
* Payload Efficiency
* Scientific Yield per Cost
* Resource Utilization Metrics

---

## 🏗 Data Model

The dashboard follows a **Star Schema** design.

### Fact Table

* Fact_SpaceMissions

### Dimension Tables

* Dim_Date
* Dim_LaunchVehicle
* Dim_MissionType
* Dim_Target
* Dim_Mission

### Benefits

* Improved report performance
* Simplified DAX calculations
* Better scalability
* Efficient filtering and slicing

---

## 📈 DAX Measures

Key DAX measures implemented include:

```DAX
Total Missions =
COUNTROWS(Fact_SpaceMissions)
```

```DAX
Successful Missions =
CALCULATE(
    [Total Missions],
    Fact_SpaceMissions[Outcome] = "Success"
)
```

```DAX
Avg Success Rate =
DIVIDE(
    [Successful Missions],
    [Total Missions]
)
```

```DAX
Average Mission Cost =
AVERAGE(Fact_SpaceMissions[Mission Cost])
```

```DAX
Cost Per Distance =
DIVIDE(
    SUM(Fact_SpaceMissions[Mission Cost]),
    SUM(Fact_SpaceMissions[Distance from Earth])
)
```

Additional measures include:

* Partial Success Missions
* Success Rate YoY
* Yield per Cost
* Average Fuel Consumption
* Average Payload
* Best Vehicle Success Rate
* Worst Vehicle Success Rate
* Best Mission Type
* Highest Yield Mission Type

---

## 🔍 Key Insights

* Average mission success rate exceeds 92%.
* Launch vehicles show significant differences in operational performance.
* Scientific yield varies considerably across mission types.
* Fuel consumption and payload capacity strongly influence mission costs.
* Cost efficiency can be improved through optimized vehicle selection.
* Long-term trend analysis reveals periods of performance fluctuations and cost spikes.

---

## 🛠 Tools & Technologies

* Power BI Desktop
* DAX
* Power Query
* Data Modeling
* Star Schema Design
* GitHub Pages

---

## 💡 Skills Demonstrated

* Data Cleaning & Transformation
* Data Modeling
* Star Schema Implementation
* DAX Measure Development
* Dashboard Design
* KPI Development
* Data Visualization
* Business Intelligence Reporting
* Insight Generation

---

## 📷 Dashboard Preview

The repository includes screenshots of:

* Overview Dashboard
* Mission Trend Analysis
* Vehicle Analysis
* Mission Type Analysis
* Cost & Resource Analysis
* Data Model Diagram

---

## 📂 Repository Contents

```text
Space-Mission-Failure-Analysis/
│
├── Dashboard Screenshots
├── Data Model Diagram
├── README.md
├── Space_Mission_Dashboard.pbix
└── Project Website
```

---

## 👨‍💻 Author

**Amithesh T S**

Machine Learning Engineer | Data Analyst | AI Enthusiast

GitHub: https://github.com/Amithesh10
LinkedIn: https://www.linkedin.com/in/amithesh-ts

---

⭐ If you found this project useful, consider giving the repository a star.
