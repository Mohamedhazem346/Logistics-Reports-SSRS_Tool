# 🚚 Logistics Analytics System: End-to-End Data Engineering & BI Solution

[![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)](https://www.microsoft.com/en-us/sql-server)
[![SSRS](https://img.shields.io/badge/SSRS_Reports-F25022?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/sql/reporting-services/)
[![n8n](https://img.shields.io/badge/n8n_Automation-FF6C37?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io/)
[![OpenAI](https://img.shields.io/badge/OpenAI_GPT--4o-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)

An enterprise-grade, end-to-end data platform built for a multi-state logistics corporation. This system seamlessly integrates robust **Data Warehousing**, pixel-perfect enterprise **SSRS Reporting**, interactive **Power BI Dashboards**, and an **Agentic AI Workflow** to transform fragmented operational data into actionable strategic insights.

---

## 🎯 Project Overview

This project addresses the modern data challenges of a logistics enterprise managing a fleet of **121 trucks**, **151 drivers**, and over **85,000 operational trips**. The solution converts raw operational data into high-performance analytical assets using a **Galaxy Schema Data Warehouse**, paired with enterprise-level **SSRS reports** for operational compliance, and an automated **n8n AI Agent** that dynamically translates natural language queries into executable SQL code, sending automated insights via Telegram and Email.

---

## 🏗️ Architecture & Data Pipelines

[Operational DB: 9 Tables] ──(SSIS ETL Process)──> [Galaxy Schema Data Warehouse]
│
┌────────────────────────────────────────────────┴──────────────────────────────┐
▼                                                ▼                              ▼
[SSRS Pixel-Perfect Reports]                 [Power BI Dashboards]          [n8n AI Agent Framework]
(Compliance & Details)                       (Strategic Analytics)         (Natural Language to SQL)


### 1. Relational Operational Database
Comprises **9 fully normalized tables** containing high-volume records:
* **Trips & Loads:** ~85,000 transactional records tracking freight movement.
* **Core Entities:** Drivers (151), Trucks (121), Customers (200), Routes (58), Facilities (50).
* **Maintenance & Logs:** 3,000+ maintenance records & 156.7K distinct delivery events.

### 2. Data Warehouse Design
Optimized for heavy analytical aggregations via a complex **Galaxy Schema (Multiple Facts Linked to Shared Dimensions)**:
* **Fact Tables:** `fact_trips`, `fact_loads`, `fact_deliveryevents`, `fact_maintenance`, `fact_drivermonthlymetrics`.
* **Dimension Tables:** `Dim_Drivers`, `Dim_Trucks`, `Dim_Customers`, `Dim_Routes`, `Dim_Facilities`, `Dim_Date`.

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

## 🤖 Agentic AI & Automation Workflow

This project introduces an autonomous **Data AI Agent** built using **n8n orchestration** to handle complex requests seamlessly:

1. **Natural Language Interface:** End-users (e.g., Logistics Managers) type questions in plain language via a **Telegram Bot** (e.g., *"Which trucks generated the highest maintenance costs last month?"*).
2. **Text-to-SQL Conversion:** The query is routed to **OpenAI GPT-4o / Codex** models embedded with the **Data Warehouse Schema Context** and strict system guardrails to prevent hallucinations.
3. **Execution & Generation:** The system dynamically writes and executes secure PostgreSQL queries hosted on the Supabase cloud data warehouse.
4. **Automated Delivery:** The generated analytical table or insight is formatted on-the-fly and emailed directly to the manager via **Google API Integration**, or replied back instantly inside the chatbot.
5. **Error Resilience:** Features a dedicated connected sub-workflow handling database timeout or syntax errors autonomously to maintain high reliability.

---

## ⚙️ Tech Stack & Prerequisites

* **Database Engine:** Microsoft SQL Server (On-Premises) & PostgreSQL (Cloud via Supabase).
* **ETL/ELT:** Microsoft SQL Server Integration Services (SSIS).
* **Reporting & Dashboards:** SQL Server Reporting Services (SSRS), Microsoft Power BI Desktop.
* **AI & Automation:** n8n Workflow Manager (Docker/Self-hosted), OpenAI API (`gpt-4o` & `Codex`).
* **Version Control:** Git & GitHub.

---

## 👥 Project Team

This project was developed by an agile team within the **Information Technology Institute (ITI)** - Power BI Track (Class of 2026):
* **Mohamed Hazem Abdelhady** - *BI Specialist (SSRS Reports Design, Data Warehousing, Modeling)*
* **Abdulrahman Mohamed Zaki** - *Data Analysis & Agentic AI Specialist*
* **Mahmoud Saeed Abdelghafar** - *BI & ETL Engineer*
* **Mohamed Abdeen Mostafa** - *Data Analyst*
* **Mostafa Mahmoud Zaghloul** - *Data Analyst*

---
*Developed as part of the ITI Graduation Project requirements for elite business intelligence standards.*
