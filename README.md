# 🚢 Titanic Dataset - Exploratory Data Analysis (EDA)

![Python](https://img.shields.io/badge/Python-3.12-blue?style=flat&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-v2.0+-150458?style=flat&logo=pandas)
![Data Analysis](https://img.shields.io/badge/Task-Data_Cleaning_&_EDA-orange)

This repository contains a comprehensive **Exploratory Data Analysis (EDA)** and **Data Cleaning** notebook for the famous Titanic dataset. The goal of this project is to explore the factors that influenced passenger survival rates and prepare the data for further predictive modeling.

---

## 📌 Project Overview

The notebook walks through the initial stages of a data science pipeline, focusing heavily on understanding data distributions, statistical summary, and treating missing values and outliers effectively.

### Key Lifecycle Steps Covered:
* **Data Loading & Inspection:** Understanding shapes, data types, and initial structures[cite: 1].
* **Data Cleaning:** Handling missing values in `Age`, `Cabin`, and `Embarked` columns using advanced contextual logic[cite: 1].
* **Outlier Analysis:** Detection of extreme values in features like `Fare` using statistical visualization[cite: 1].
* **Data Visualization:** Leveraging modern libraries for plotting and insight generation[cite: 1].

---

## 🛠️ Tech Stack & Libraries

* **Language:** Python 3.12[cite: 1]
* **Data Manipulation:** `pandas`, `numpy`[cite: 1]
* **Data Visualization:** `matplotlib`, `seaborn`, `plotly.express`, `plotly.graph_objects`[cite: 1]

---

## 📊 Dataset Insights & Observations

### Initial Shape
The dataset consists of **891 rows** and **12 columns**[cite: 1].

### Missing Data Summary:
* **Cabin:** Missing **77.1%** of data (687 values)[cite: 1].
* **Age:** Missing **19.8%** of data (177 values)[cite: 1].
* **Embarked:** Missing **0.2%** of data (2 values)[cite: 1].

### Core Observations:
1. **Survival Rate:** Around **38.3%** of the passengers in this dataset survived[cite: 1].
2. **Fare Outliers:** The maximum fare ($512.33$) is significantly higher than the average fare ($32.20$), indicating the presence of extreme outliers from ultra-wealthy first-class passengers[cite: 1].
3. **Age Distribution:** Passenger ages range from infants (0.42 years) up to 80 years, with a median age of around 28–29 years[cite: 1].

---

## 🧼 Data Cleaning Approach

* **`Embarked` Column:** Filled the 2 missing values with the **Mode ('S')** since it is the most frequent port[cite: 1].
* **`Age` Column:** Implemented **Contextual Grouped Imputation**. Instead of a global median, missing ages were filled based on the specific median of the passenger's class (`Pclass`) and gender (`Sex`) to maintain a realistic distribution[cite: 1].
* **`Cabin` Column:** Dropped completely due to the severe lack of data (77% missing), preventing noise injection[cite: 1].

---

## 🚀 How to Run the Notebook

1. Clone this repository:
```bash
   git clone [https://github.com/your-username/titanic-eda.git](https://github.com/your-username/titanic-eda.git)
