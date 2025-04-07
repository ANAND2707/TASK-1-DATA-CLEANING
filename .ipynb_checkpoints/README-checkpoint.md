
# 🧹 Task 1 - Data Cleaning

This project involves cleaning and preprocessing a medical appointment dataset to prepare it for analysis and modeling.

---

## 📁 Folder Structure

TASK-1-DATA-CLEANING/
├── rawdata/
│   └── KaggleV2-May-2016.csv
├── cleaned_dataset.csv               ← Generate this in notebook
├── data_cleaning.ipynb               ← Main code notebook
├── README.md                         ← Short explanation of your work
└── screenshots/
    ├── before_head.png
    ├── before_info.png
    ├── after_head.png
    └── after_info.png


---

## ✅ Data Cleaning Checklist

| Step | Task                       | Description |
|------|----------------------------|-------------|
| ✅ 1 | `df.head()`                | Preview raw data |
| ✅ 2 | `df.info()`                | Understand structure & data types |
| 🔍 3 | Graphs Before Cleaning     | Show distribution, outliers |
| 🔎 4 | `df.isnull().sum()`        | Checked for missing values |
| ✂️ 5 | `df.drop_duplicates()`     | Removed duplicates |
| 🎯 6 | **Standardize Data**        | Cleaned key columns (see below) |
| 🕒 7 | Fix Date Columns           | Converted `ScheduledDay`, `AppointmentDay` to `datetime` |
| 🏷️ 8 | Rename Columns             | Fixed typos like `No-show` → `No_Show`, `Handcap` → `Handicap` |
| 🔎 9 | Check Data Types           | Verified all types post-cleaning |
| 🚫 10 | Fix Outliers / Negatives  | Fixed invalid `Age < 0`, and `Handicap > 4` |
| 🧪 11 | `No_Show` to 0/1          | Binary encoding for ML use |
| 💾 12 | Save Cleaned Dataset      | Used `to_csv()` to export cleaned data |
| 📊 13 | Graphs After Cleaning     | Compared cleaned vs raw visuals |

---

## 🧼 Standardized Columns

### 1. `Gender`

We cleaned the `Gender` column to make it more readable and consistent.

- **Before**: `['M', 'F']`
- **After**: `['Male', 'Female']`

**Why this change?**

- Ensures full, human-readable labels.
- Helps in filtering, grouping, and visualization.
- Improves clarity when shared with others or used in plots.

---

### 2. `No_Show`

We made the `No_Show` column more interpretable by renaming values.

- **Before**: `['No', 'Yes']`
- **After**: `['Showed Up', 'Missed']`

**Why this change?**

- Makes the data human-readable.
- Clearly reflects what the values mean.
- Easier to understand when modeling or making charts.

---

## 🔢 Fixing Large IDs

We converted columns like `PatientID` and `AppointmentID` from numeric types to strings.

**Why this change?**

- Prevents Excel or CSV viewers from converting them into scientific notation (e.g., `2.98E+13`).
- Preserves the integrity of long IDs without truncation.
- Keeps values consistent when sharing or visualizing data.

---

## 📌 Dataset Source

- Medical Appointment No Shows | Kaggle:  
  https://www.kaggle.com/datasets/joniarroba/noshowappointments

---
