# 🚚 Logistics Analytics System: End-to-End Data Engineering & BI Solution

[![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)](https://www.microsoft.com/en-us/sql-server)
[![SSRS](https://img.shields.io/badge/SSRS_Reports-F25022?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/sql/reporting-services/)
[![n8n](https://img.shields.io/badge/n8n_Automation-FF6C37?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io/)
[![OpenAI](https://img.shields.io/badge/OpenAI_GPT--4o-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)

An enterprise-grade, end-to-end data platform built for a multi-state logistics corporation. This system seamlessly integrates robust **Data Warehousing**, pixel-perfect enterprise **SSRS Reporting**, interactive **Power BI Dashboards**, and an **Agentic AI Workflow** to transform fragmented operational data into actionable strategic insights.

--- 

## 📊 SSRS Enterprise Reports Details

The `Reports/` directory contains standard definition corporate reports (`.rdl`) developed via **Microsoft SQL Server Reporting Services (SSRS)**. These reports are engineered for operational monitoring, compliance, and pixel-perfect printing format.

### 1. Trips Details Report (`Trips Details Report.rdl`)
* **Objective:** Comprehensive tracking of dispatch lifecycle and financial health per trip.
* **Key Metrics Covered:** Total Trip Cost, Revenue Generated, Profit Margin, Breakdown of Late vs. On-time Deliveries.
* **Visual Elements:** Spatial analysis utilizing integrated charts, grouped breakdown by shipping Route, and conditional status formatting.

### 2. Trucks Operational Performance (`Trucks Details Report.rdl`)
* **Objective:** Fleet health optimization, monitoring utilization and maintenance overheads.
* **Key Metrics Covered:** Total Miles Traveled, Odometer milestones, Maintenance cost distribution, and Fuel Efficiency metrics.
* **Features:** Conditional alerts for trucks exceeding critical maintenance cost thresholds or showing low utilization rates.

### 3. Driver Performance Analytics (`Driver Performance.rdl`)
* **Objective:** Evaluating operator behavior, efficiency, and safety compliance.
* **Key Metrics Covered:** Safety compliance scores, Avg Delay Times per driver, Completed Trips vs. Cancelled Trips, and Monthly Performance ranking.
* **Features:** Interactive Drill-down parameters allowing managers to evaluate specific drivers within chosen regions.

### 4. Customer & Revenue Report (`Customer_Report.rdl`)
* **Objective:** Identifying high-value accounts and regional revenue distributions.
* **Key Metrics Covered:** Customer Lifetime Value (CLV), Active order counts, and regional distribution of load weights.

---
