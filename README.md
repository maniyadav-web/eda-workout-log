# Fitness Data Cleaning & Analysis 🏋️‍♂️📊

A Python-based data preprocessing and exploratory data analysis (EDA) project that transforms a messy, real-world fitness dataset into structured, clean data ready for analysis.

## 📌 Project Overview
This project showcases essential data-cleaning techniques using the Python `Pandas` library. Real-world health and workout data often arrives with missing records, incorrect tracking formats, or human-input typos. This script targets and fixes those issues to create accurate, reliable visualizations.

## 🛠️ Data Anomalies Handled
Using an initial data audit (`df.info()` and `df.isnull()`), the following issues were discovered and resolved:
* **Inconsistent Date Formats:** Standardized literal single quotes and unformatted date entries (e.g., `20201226`) using `pd.to_datetime(format='mixed')`.
* **Missing Records:** Automatically dropped rows completely missing a `Date` entry, and safely imputed missing `Calories` cells using the column's median value ($291.2\text{ kcal}$).
* **Data Entry Outliers:** Caught and corrected a manual input typo where a workout duration was logged as $450$ minutes instead of $45$ minutes.
* **Duplicate Values:** Decluttered the dataset by identifying and removing identical, duplicated rows.

## 📈 Key Insights Discovered
* **Habit Tracking:** The user heavily favors $60\text{-minute}$ workout blocks over $30$ or $45\text{-minute}$ sessions.
* **Heart Rate Correlation:** A strong linear correlation exists between average resting workout pulse and peak pulse (`Maxpulse`).
* **Energy Burn:** Calorie expenditures steadily fluctuated between $200\text{ kcal}$ and $480\text{ kcal}$ based on the intensity and length of the workout.

## 🚀 Tech Stack Used
* **Language:** Python
* **Libraries:** Pandas (Data manipulation), Matplotlib (Data Visualization)
