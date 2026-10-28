# 🚗 Mercedes-Benz Data Analysis & Interactive Dashboard | Python

## Project Overview
This project performs an end-to-end data analysis on a Mercedes-Benz pre-owned cars dataset using **Python (Pandas, NumPy, Matplotlib, Seaborn, and Plotly)**. The primary objective is to clean messy raw data, handle missing values and outliers, explore relationships between car features, and build a fully interactive dark-themed analytics dashboard.

---

## 📊 Dataset Description
The dataset (`mercedes_cars.csv`) features listing records for various Mercedes-Benz models with the following core attributes:

| Column | Description |
| :--- | :--- |
| **model** | Mercedes-Benz car model (e.g., C-Class, S-Class, A-Class, GLC, CLA) |
| **year** | Manufacturing year of the vehicle |
| **price_eur** | Listing price in Euros (€) |
| **mileage_km** | Total distance driven in kilometers |
| **fuel_type** | Engine fuel classification (Petrol, Diesel, Hybrid) |
| **transmission** | Transmission mechanism (Automatic, Manual) |
| **engine_size_l** | Engine displacement capacity in liters |
| **horsepower** | Vehicle engine power output (HP) |
| **previous_owners** | Number of past vehicle owners |

---

## 🛠️ Tools & Libraries Used
* **Python 3.x**
* **Pandas & NumPy:** Data wrangling, missing value imputation, and IQR outlier capping.
* **Matplotlib & Seaborn:** Exploratory Data Analysis (EDA) and distribution plots.
* **Plotly (Express & Graph Objects):** Custom multi-panel interactive dark-themed HTML dashboard (`plotly_dark`).
* **VS Code / Jupyter Notebook**

---

## 🔄 Project Workflow & Methodology

1. **Data Understanding & Inspection:** Inspected dataset shape, data types, duplicate counts, and structural completeness.
2. **Data Cleaning & Preprocessing:** 
   * Removed duplicate records using `drop_duplicates()`.
   * Imputed missing numerical variables using **medians** and categorical variables using **modes**.
   * Applied **IQR Capping** to handle extreme outliers in numerical columns (`price_eur`, `mileage_km`, etc.).
3. **Exploratory Data Analysis (EDA) & Dashboard Architecture:**
   * Built a 6-chart grid layout interactive dashboard showcasing historical price trends, price by model, mileage vs. price correlation, fuel type share, and horsepower distribution.
4. **KPI Summary:** Highlighted core metrics at the top of the dashboard (Total Market Price ~$135.5M, Average Mileage ~81.1k km, Average Previous Owners).

---

## 💡 Key Insights
* **Mileage Depreciation:** Strong inverse correlation observed between vehicle mileage and listing price—higher mileage listings systematically record lower market valuations.
* **Model Valuation:** Flagship luxury lines (like S-Class and AMG-GT) retain significantly higher median resale values compared to entry-tier models.
* **Fuel Type & Performance:** Diesel and Petrol dominate listings, while Hybrids show distinct modern valuation trends.

---

## ⚠️ Limitations
* **Imputation Impact:** Median imputation preserves distribution centers but slightly compresses tail variance.
* **Correlation vs. Causation:** Correlation between mileage and price reflects market association rather than strict single-factor causality.

---

## 🎯 Business Value
* **Pricing Strategy Optimization:** Empowers dealerships and pricing teams with data-driven benchmarking for pre-owned vehicle valuations.
* **Inventory Insights:** Delivers clear visibility into model demand and customer fuel preferences.

---

## Skills Demonstrated
* Data Cleaning (missing values, duplicates, IQR outlier treatment)
* Data Analysis with Pandas (groupby, value counts, filtering)
* Correlation Analysis
* KPI Calculation & Dashboard Design
* Interactive Data Visualization (Plotly)
* Insight Communication

---

## 🚀 How to Run
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/mohamed-gouda74/mercedes_dashboard.git](https://github.com/mohamed-gouda74/mercedes_dashboard.git)
