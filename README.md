# Unified_Mentor_Nassau_Candy_Distributor_Analysis

# Factory-to-Customer Shipping Route Efficiency Analysis
**Data Analyst Internship Project — Unified Mentor**

An end-to-end supply chain analytics pipeline and exploratory data analysis (EDA) project evaluating order fulfillment efficiency, shipping lead times, and regional bottlenecks for **Nassau Candy Distributor**.

---

## 📋 Project Overview
Managing high-volume wholesale distribution networks requires rigorous, data-driven optimization to minimize transit times, reduce fulfillment delays, and optimize freight routes. This project processes a comprehensive enterprise transactional dataset of **10,194 records** to analyze supply chain performance across multiple manufacturing plants and nationwide customer destinations. 

The analysis was fully developed and executed inside **Google Colab** using Python, transforming raw operational logs into actionable Key Performance Indicators (KPIs) and route-level insights.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3 (64-bit)
* **Environment:** Google Colab / Jupyter Notebook
* **Data Manipulation & Analysis:** `pandas`, `NumPy`
* **Data Visualization:** `Matplotlib`, `Seaborn`
* **Version Control:** Git & GitHub

---

## 📂 Project Architecture & Pipeline
1. **Environment Setup & Data Ingestion:** Loaded the transactional dataset (`10,194` rows, `18` columns) containing order IDs, customer details, timestamps, geographical attributes, and financial metrics.
2. **Data Cleaning & Hygiene:** 
   * Converted `Order Date` and `Ship Date` columns into proper datetime objects.
   * Filtered out data anomalies (e.g., negative lead times where delivery preceded order placement).
   * Standardized geographical strings (city, state, region) to eliminate grouping inconsistencies caused by whitespace or casing.
3. **Feature Engineering:** Created core operational metrics such as **Shipping Lead Time** (delta between order date and ship date in days).
4. **Exploratory Data Analysis (EDA) & Aggregation:** Grouped shipments by delivery corridors (`Region` $\rightarrow$ `State/Province` $\rightarrow$ `Ship Mode`) to compute:
   * Total Shipment Volumes
   * Mean and Standard Deviation of Lead Times
   * Delay Frequencies (percentage of orders exceeding a 5-day delivery threshold)

---

## 📊 Key Findings & Empirical Results
* **Global Baseline:** The overall average shipping lead time across all standard channels was established at **4.40 days**.
* **Regional Bottlenecks:** Subset analysis on the *Interior Region* under *Standard Class* shipping revealed an average lead time of **5.49 days**, with over **43% of orders** experiencing delays beyond the 5-day service threshold.
* **Shipping Mode Performance:** Expedited tiers (*First Class* / *Same Day*) demonstrated stable transit durations (~2–3 days) with minimal variance, whereas *Standard Class* exhibited high tail-end dispersion and vulnerability to geographic congestion.

---

## 🚀 Repository Structure
```text
├── data/                      # Raw and cleaned enterprise datasets
├── notebooks/                 # Google Colab Jupyter notebooks (.ipynb)
├── reports/                   # Comprehensive technical documentation & PDF reports
└── README.md                  # Project documentation
