# Employee Data Insights (SQL)

## 📌 Project Overview
This repository contains a collection of advanced SQL scripts designed to analyze human resources, payroll, and departmental data structure models. The queries solve real-world analytical problems—such as mapping organizational hierarchies, calculating payroll distributions, and identifying salary disparities—using advanced relational algebra.

Additionally, this project includes comprehensive relational database analysis using the standard **Sakila** schema to trace customer behaviors and inventory trends across global regions.

---

## 🛠️ Tech Stack & Database Environments
* **Language:** SQL (Structured Query Language)
* **Dialect Compatibility:** MySQL, PostgreSQL, MS SQL Server
* **Target Schemas:** * Custom Core HR/Payroll Tables (`EMP` & `EMP_SAL`)
  * Sakila DVD Rental Database Schema

---

## 📊 Core Analytical Insights & Core Queries

### 1. Human Resources & Disparity Analytics (Self-Joins)
Self-joins are a critical technique used to compare rows within the same table. This section addresses deep organizational questions:
* **Peer-to-Peer Matching:** Finding exact pairs of employees sharing identical designations, salaries, or physical locations while strictly filtering out duplicate pairings (`e1.eid < e2.eid`).
* **Compensational Skew Tracking:** Identifying specific employees who earn significantly more than their direct department's average using nested subquery isolation.
* **Internal Pay Disparities:** Isolating distinct employee pairings within identical business sectors where a salary gap greater than ₹50,000 exists.

### 2. Micro & Macro Financial Metrics (Window Functions)
Window functions allow complex metrics to be computed across groups of rows without collapsing detail records:
* **Running Totals:** Implementing sequential running salary calculations (`SUM() OVER`) partitioned by department and ordered by Employee ID (`eid`).
* **Relative Contribution Analysis:** Calculating the exact mathematical percentage contribution an individual's salary adds to their group's overall department budget.
* **Sequential Trend Gaps:** Using `LAG()` over partitioned datasets to calculate the immediate, step-by-step financial difference between employee salaries sorted by identification numbers.

### 3. Cross-Relational Retail Analytics (Sakila Model)
Demonstrates multi-table traversal capabilities by linking **Category**, **Film**, **Inventory**, **Rental**, **Customer**, **Address**, and **City** structures to evaluate product distribution densities by geographical market.

---
