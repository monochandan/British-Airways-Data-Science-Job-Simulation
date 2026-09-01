# British Airways Data Science Job Simulation (Forage)

[![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Excel](https://img.shields.io/badge/Excel-Modeling-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://www.microsoft.com/en-us/microsoft-365/excel)
[![pandas](https://img.shields.io/badge/pandas-Data%20Prep-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-Machine%20Learning-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=for-the-badge&logo=plotly&logoColor=white)](https://matplotlib.org/)
[![PowerPoint](https://img.shields.io/badge/PowerPoint-Reporting-B7472A?style=for-the-badge&logo=microsoftpowerpoint&logoColor=white)](https://www.microsoft.com/en-us/microsoft-365/powerpoint)
[![Forage](https://img.shields.io/badge/Forage-Job%20Simulation-6236FF?style=for-the-badge&logo=forage&logoColor=white)](https://www.theforage.com/)
![License](https://img.shields.io/badge/license-MIT-green)

British Airways Data Science Job Simulation (Forage): Built an Excel lookup model estimating lounge eligibility across flight groupings (Task 1), and a Python Random Forest model predicting customer booking behavior with feature importance analysis and stakeholder reporting (Task 2).

## 📌 Overview

This repository contains my solutions to Forage's British Airways Data Science Job Simulation, split into two tasks:

- **Task 1:** Lounge Eligibility Lookup Template - Task 1.xlsx
- **Task 2:** EDA.ipynb, prepare_data_for_model_training.ipynb 

---

## ✈️ Task 1: Modeling Lounge Eligibility

**Goal:** Build a reusable lookup table estimating what proportion of passengers in a given flight category are eligible for each of BA's three lounge tiers (Tier 1 – Concorde Room [hypothetical], Tier 2 – First Lounge, Tier 3 – Club Lounge), based on a 10,000-flight summer schedule dataset.

**Approach:**
- Explored the flight schedule dataset (10,000 flights) covering route, region, haul type, time of day, aircraft type, and seat configuration
- Tested multiple grouping strategies (Haul + Time of Day, Haul + Region, Haul + Aircraft Type) to identify which best explained variation in lounge eligibility
- Selected **Haul Type + Time of Day** as the final model — it captured meaningful variation while remaining simple and always knowable at the schedule-planning stage
- Built a reusable **Category → Tier 1/2/3 %** lookup table and applied it to a sample of individual flights to estimate lounge demand
- Documented assumptions, methodology, and limitations in a written justification

**Deliverable:** `Lounge Eligibility Lookup Template - Task 1.xlsx`

**Tools:** Excel (SUMIFS, VLOOKUP/INDEX-MATCH, PivotTables, charts)

---

## 🎯 Task 2: Predicting Customer Buying Behaviour

**Goal:** Build a machine learning model to predict whether a customer completes a booking, and identify which factors most influence purchase decisions — enabling BA to proactively target likely customers before they travel.

**Approach:**
- Explored and cleaned the customer booking dataset
- Engineered new features to improve predictive power
- Trained a **Random Forest classifier** (chosen for its interpretable feature importance output)
- Evaluated performance using cross-validation and metrics including accuracy, precision, recall, and ROC-AUC
- Visualized feature importance to explain what drives booking behavior
- Summarized results in a single, manager-ready PowerPoint slide

**Deliverables:**
- `Prediction Customer Booking Completion - Model Summary.pptx`


**Tools:** Python (pandas, scikit-learn, matplotlib/seaborn)

---


## 🛠️ Repository Structure

```
    ├── Task 1 Modeling lounge eligibility at Heathrow Terminal 3/
    │   └── British Airways Summer Schedule Dataset - Forage Data Science Task 1.xlsx (Task analysis)
    |   └── Lounge Eligibility Lookup Template - Task 1.xlsx (Final Submission)
    └── Task2/
        ├── EDA.ipynb
        └── prepare_data_for_model_training.ipynb
        └── Prediction Customer Booking Completion - Model Summary.pptx (Final Submission)
└── README.md
```

---

## 🎓 About

Completed as part of the **British Airways Data Science Job Simulation** on [Forage](https://www.theforage.com/).
