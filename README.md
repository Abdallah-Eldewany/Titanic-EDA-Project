# 📊 Data Cleaning with Pandas (GroupBy + Transform)

## 🧠 Overview
This notebook demonstrates how to clean missing data in a dataset using advanced Pandas techniques, specifically:

- `groupby()`
- `transform()`
- `lambda functions`
- `fillna()` with median imputation

The focus is on handling missing values in a smart way instead of using global averages.

---

## 🎯 Problem Statement
The dataset contains missing values in the **Age** column. Instead of filling all missing values with a single global value, we aim to improve accuracy by filling missing ages based on similar groups of passengers.

We group the data by:
- Passenger class (`Pclass`)
- Gender (`Sex`)

---

## ⚙️ Technique Used

### 📌 Group-Based Imputation
We use the median age within each group (Pclass + Sex) to fill missing values.

### 💡 Key Code
```python
df['Age'] = df.groupby(['Pclass', 'Sex'])['Age'].transform(
    lambda x: x.fillna(x.median())
)
