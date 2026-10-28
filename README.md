# 🚗 Mercedes-Benz Data Analysis & Interactive Dashboard | Python

## Project Overview
This project performs an end-to-end data analysis on a Mercedes-Benz pre-owned cars dataset using **Python (Pandas, NumPy, Matplotlib, Seaborn, and Plotly)**. The primary objective is to clean messy raw data, handle missing values and outliers, explore relationships between car features (model, mileage, price, fuel type, horsepower), and build a fully interactive dark-themed analytics dashboard.

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
* **Pandas & NumPy:** Data wrangling, missing value imputation, IQR outlier capping, and feature transformation.
* **Matplotlib & Seaborn:** Exploratory Data Analysis (EDA) and distribution visualizations (Histograms, Boxplots).
* **Plotly (Express & Graph Objects):** Custom multi-panel interactive dark-themed HTML dashboard (`plotly_dark`).
* **VS Code / Jupyter Notebook**

---

## 🔄 Project Workflow & Methodology

### 1. Data Understanding & Inspection
* Inspected dataset shape, data types, duplicate counts, and structural completeness using `.info()`, `.describe()`, and `.isnull().sum()`.

### 2. Data Cleaning & Preprocessing
* **Duplicate Removal:** Identified and dropped duplicate listings using `drop_duplicates()`.
* **Missing Value Imputation:**
  * Imputed missing numerical variables (`price_eur`, `mileage_km`, `engine_size_l`, `horsepower`, `previous_owners`) using their respective column **medians**.
  * Imputed missing categorical columns (`transmission`, `fuel_type`) using their statistical **mode**.
* **Outlier Capping (IQR Method):**
  * Calculated Interquartile Range ($IQR = Q3 - Q1$) across numerical columns.
  * Applied upper and lower boundary capping via `.clip()` to manage extreme variance without dropping observation rows.
* **Column Standardization:** Renamed features for consistent analysis mapping (`fuel_type` $\rightarrow$ `fuelType`, `mileage_km` $\rightarrow$ `mileage`).

### 3. Exploratory Data Analysis (EDA) & Dashboard Architecture
* Constructed an interactive 6-chart grid layout dashboard using Plotly subplots (`plotly_dark` theme):
  1. **Avg Price Over Year:** Bar chart evaluating historical vehicle pricing trends.
  2. **Total Price by Model:** Trend visualization mapping valuation distribution across models.
  3. **Price vs Mileage:** Interactive scatter plot displaying negative price degradation relative to driven distance.
  4. **Fuel Type Share:** Donut/Pie visual tracking Petrol, Diesel, and Hybrid model proportions.
  5. **Price vs KM Gauge/Visuals:** Performance metrics comparing driven distance against market value.
  6. **Horsepower Distribution:** Performance gauge visual capturing engine HP spread.

### 4. KPI Summary
Key aggregated metrics showcased at the header of the interactive dashboard:
* **Total Market Price:** ~$135.5M
* **Average Mileage:** 81.1k km
* **Average Previous Owners:** 2 Owners

---

## 💡 Key Insights
* **Mileage Depreciation:** Strong inverse correlation observed between vehicle mileage (`mileage_km`) and listing price (`price_eur`)—higher mileage listings systematically record lower market valuations.
* **Model Valuation:** Flagship luxury lines like S-Class and AMG-GT retain significantly higher median resale values compared to entry-tier A-Class and CLA models.
* **Fuel Type Distribution:** Diesel and Petrol variants dominate pre-owned listings, with Hybrid models steadily gaining market representation in recent year models.
* **Owner Impact:** Vehicles with single previous ownership maintain higher price resilience compared to vehicles with 3+ prior owners.

---

## ⚠️ Limitations
* **Imputation Smoothing:** Median imputation preserves distribution medians but slightly compresses variance in tail distributions.
* **Correlation vs. Causation:** The correlation between mileage, vehicle year, and price reflects market association rather than strict single-factor causality.

---

## 🎯 Business Value
* **Pricing Strategy Optimization:** Provides dealership networks and pricing teams with empirical benchmarking for pre-owned valuation based on mileage, age, and horsepower.
* **Inventory Allocation:** Enables clear visibility into high-demand models, fuel preferences, and sweet spots for inventory acquisition.

---

## ⚙️ How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/mohamed-gouda74/mercedes_dashboard.git](https://github.com/mohamed-gouda74/mercedes_dashboard.git)
   cd mercedes_dashboard
