# 🚗 Mercedes-Benz Analytics & Interactive Dashboard

An end-to-end data analysis and interactive dashboard project built in Python, leveraging powerful data manipulation and visualization libraries to analyze Mercedes-Benz car listings, pricing trends, and vehicle specifications.

---

## 📊 Project Overview
This project processes a dataset of Mercedes-Benz vehicles to uncover insights regarding vehicle pricing, mileage distribution, fuel efficiency, and model performance. Using **Python**, **Pandas**, and **Plotly**, an interactive multi-panel dashboard was designed with a custom dark mode aesthetic to provide a seamless analytical experience.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Processing & Cleaning:** Pandas, NumPy
* **Data Visualization & Dashboarding:** Plotly (Express & Graph Objects), Matplotlib, Seaborn
* **Environment:** Jupyter Notebook / VS Code

---

## 🔍 Key Data Pipeline Steps
1. **Data Loading & Inspection:** Loaded the Mercedes dataset and checked for data types, missing values, and structure.
2. **Data Cleaning:** 
   * Handled and dropped duplicate records.
   * Imputed missing numerical values using medians and categorical values using modes.
3. **Outlier Treatment:** Applied Interquartile Range (IQR) capping to numerical features (`price_eur`, `mileage_km`, `horsepower`, etc.) to stabilize distributions.
4. **Feature Engineering & Renaming:** Standardized columns and prepared metrics for dashboard aggregation.

---

## 📈 Dashboard Features (`Mercedes Analytics Dashboard`)
The interactive Plotly dashboard features a sleek dark mode theme (`plotly_dark`) displaying:
* **KPI Cards:** Total Market Price (`$135.5M`), Average Mileage (`81.1k km`), and Average Previous Owners.
* **Price Analysis:** Breakdown of average prices across manufacturing years and models.
* **Mileage vs. Price:** Interactive scatter plot visualizing the correlation between vehicle mileage and listing price across various models.
* **Fuel Type & Horsepower Distribution:** Visual proportions of fuel types and engine performance metrics.

---

## 🚀 How to Run
1. Clone the repository or open the notebook in VS Code / Jupyter Notebook.
2. Ensure required libraries are installed:
   ```bash
   pip install pandas numpy matplotlib seaborn plotly
