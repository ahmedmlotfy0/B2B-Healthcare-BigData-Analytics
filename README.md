# 🏥 B2B Healthcare Analytics & Big Data Optimization

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Memory_Optimized-green.svg)
![Data](https://img.shields.io/badge/Dataset-24M+_Rows-orange.svg)

## 📌 Project Overview
Handling and analyzing large-scale datasets efficiently is a critical challenge in modern data analytics. This project explores the **2016 Medicare Part D Prescriber dataset (over 24 Million records)** to extract strategic business intelligence regarding drug utilization, major cost drivers, and physician prescribing behaviors.

Leveraging my medical domain knowledge alongside advanced data engineering techniques, this project bridges the gap between raw healthcare data and actionable B2B pharmaceutical insights.

## ⚙️ Technical Highlights & Big Data Optimization
Processing a 1GB+ CSV file with ~25 million rows on limited computational resources (like Google Colab) requires strict memory management. I implemented the following Data Engineering strategies:

1. **Chunk-Based Processing:** Bypassed RAM limitations by reading the massive dataset in sequential chunks of `1,000,000` rows.
2. **Strategic Dtype Downcasting:** Significantly reduced memory footprint by converting standard numerical types to optimal formats (e.g., `uint32`, `uint16`, `float32` for costs and claim counts).
3. **Categorical Transformation:** Converted low-cardinality string columns (City, State, Specialty, Drug Name) into pandas `category` datatypes, minimizing object-storage overhead.
4. **Garbage Collection:** Actively managed RAM using Python's `gc.collect()` during the ETL process.

**Result:** Successfully loaded, cleaned, and analyzed the entire dataset without system crashes, proving the ability to handle enterprise-level data structures.

## 📊 Key Business Insights (Domain Expertise)

### 1. High-Volume vs. High-Value Specialties
* **Internal Medicine** ($23.7B) and **Family Practice** ($18.5B) are the undisputed leaders in total drug expenditure. This is driven by massive patient bases and high-volume prescriptions for chronic conditions.
* Conversely, **Hematology-Oncology** drives costs through *High-Value* targeted therapies, ranking 5th in total cost ($5.8B) despite a fraction of the claim volume.

### 2. Top Drugs Driving B2B Revenue
* **General Medicine:** The highest expenditures in Internal Medicine are dominated by chronic disease management drugs like **JANUVIA** ($889M), **CRESTOR** ($786M), and **LANTUS SOLOSTAR** ($753M).
* **Specialized Care:** Hematology-Oncology costs are heavily skewed by premium oncology medications, notably **REVLIMID** ($1.54B) and **IBRANCE** ($495M).

### 3. Cost Per Claim Metric
Analyzing the cost per claim exposes the financial intensity of specific treatments:
* **Hematology-Oncology** leads with a staggering average of **$999.09 per claim**.
* **General Practice** (Internal Medicine/Family Practice) averages much lower (**~$50 - $62 per claim**), highlighting the fundamental business model difference between specialized targeted therapies and mass-market pharmaceuticals.

## 🚀 How to Run the Project
1. Clone this repository:
   ```bash
   git clone [https://github.com/YourUsername/B2B-Healthcare-BigData-Analytics.git](https://github.com/YourUsername/B2B-Healthcare-BigData-Analytics.git)
