# Supplement Experiments — Data Cleaning, Integration & User Health Pipeline

This project integrates multiple datasets for **1001‑Experiments**, a company that creates personalized supplement regimens based on user health metrics, wearable data, and experiment metadata.  
The goal is to clean, standardize, and merge four separate datasets into a single unified dataset for downstream analysis.

This project was completed as part of a **DataCamp Data Engineer Practical Exam**.

---

## 🔍 Business Problem

1001‑Experiments collects data from:

- Wearable devices  
- Supplement intake logs  
- Experiment metadata  
- User demographic profiles  

Developers currently cross‑reference these datasets manually, which is inefficient and error‑prone.  
A unified dataset is required to:

- Improve experiment tracking  
- Analyze supplement effectiveness  
- Combine health metrics with supplement usage  
- Support personalized recommendations  

Your task was to write a Python function that cleans and merges all datasets into one consistent structure.

---

## 🛠️ Skills Used

- Python (Pandas, NumPy)  
- Data Cleaning & Standardization  
- Missing Value Handling  
- Type Conversion  
- Unit Conversion (mg → grams)  
- Merging Multiple Datasets  
- Feature Engineering (age groups, activity levels)  

---

## 📂 Project Tasks

### **Task — Clean & Merge All Datasets**
Using the four input files:

- `user_health_data.csv`  
- `supplement_usage.csv`  
- `experiments.csv`  
- `user_profiles.csv`  

The function `merge_all_data()` performs:

#### **1. Data Cleaning**
- Convert missing ages to `"Unknown"`  
- Convert age to standardized age groups  
- Convert supplement dosage from mg → grams  
- Replace missing supplement names with `"No intake"`  
- Handle missing experiment names  
- Clean date formats  
- Normalize sleep hour values  
- Map activity levels (1–4) to 0–100 scale  

#### **2. Merging Logic**
Merged on:

- `user_id`  
- `date`  
- `experiment_id`  

Ensures one row per user per day.

#### **3. Final Output Columns**
The final dataset includes:

- `user_id`  
- `date`  
- `email`  
- `user_age_group`  
- `experiment_name`  
- `supplement_name`  
- `dosage_grams`  
- `is_placebo`  
- `average_heart_rate`  
- `average_glucose`  
- `sleep_hours`  
- `activity_level`  

Output: **`merged_df`** dataframe.

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `Supplement Experiments.pdf` | Original DataCamp practical exam submission |
| `merge_all_data.py` | Full cleaning + merging pipeline |
| `user_health_data.csv` | Wearable + health metrics |
| `supplement_usage.csv` | Supplement intake logs |
| `experiments.csv` | Experiment metadata |
| `user_profiles.csv` | User demographic information |

---

## 🧠 Key Insights

- A unified dataset enables more accurate experiment tracking.  
- Converting dosage units and standardizing age groups improves consistency.  
- Activity level mapping creates a usable numeric feature for analysis.  
- Merging four datasets reveals gaps that were previously hidden in siloed data.  

---

## 👤 Author

**Bala Akhil Rajdeep Battula**  
Data & Technology Professional → Automotive Technology (WDTC Fall 2026)
