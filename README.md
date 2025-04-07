
# Task 1 - Data Cleaning

This project involves cleaning and preprocessing a medical appointment dataset.

## 📁 Folder Structure
TASK-1-DATA-CLEANING/
├── rawdata/
│   └── KaggleV2-May-2016.csv
├── cleaned_dataset.csv               ← Cleaned data output
├── data_cleaning.ipynb              ← Main Jupyter Notebook with code
├── README.md                        ← This file
└── screenshots/
    ├── before_head.png
    ├── before_info.png
    ├── after_head.png
    └── after_info.png

## ✅ Data Cleaning Checklist

| Step | Task | Description |
|------|------|-------------|
| ✅ 1 | df.head() | Already done |
| ✅ 2 | df.info() | Already done |
| 🔥 3 | Graphs Before Cleaning | Show data distribution, outliers, value counts |
| 🔍 4 | df.isnull().sum() | Check missing values |
| ✂️ 5 | df.drop_duplicates() | Remove duplicate rows |
| 🎯 6 | Standardize Data | Clean/format columns like Gender, No-show, etc. |
| 🕒 7 | Fix Date Columns | Convert ScheduledDay, AppointmentDay to datetime |
| 🏷️ 8 | Rename Columns | e.g., No-show → No_Show, Handcap → Handicap |
| 🔎 9 | Check Data Types | Verify after conversion |
| 🧹 10 | Fix Outliers / Negatives | e.g., Age < 0, Handcap > 4 |
| 🧪 11 | Convert No-show to 0/1 | Useful for ML/plotting |
| 💾 12 | Save Cleaned Dataset | Done using to_csv() |
| 📊 13 | Graphs After Cleaning | Same plots as Step 3 for comparison |

---

📌 Dataset Source: [Kaggle Medical Appointments Dataset](https://www.kaggle.com/datasets/joniarroba/noshowappointments)
