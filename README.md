# British Airways Data Science Job Simulation (Forage)

British Airways Data Science Job Simulation (Forage): Built an Excel lookup model estimating lounge eligibility across flight groupings (Task 1), and a Python Random Forest model predicting customer booking behavior with feature importance analysis and stakeholder reporting (Task 2).

## 📌 Overview

This repository contains my solutions to Forage's British Airways Data Science Job Simulation, split into two tasks:

- **Task 1:** Modeling Lounge Eligibility at Heathrow Terminal 3
- **Task 2:** Predicting Customer Buying Behaviour

---

## ✈️ Task 1: Modeling Lounge Eligibility

**Goal:** Build a reusable lookup table estimating what proportion of passengers in a given flight category are eligible for each of BA's three lounge tiers (Tier 1 – Concorde Room [hypothetical], Tier 2 – First Lounge, Tier 3 – Club Lounge), based on a 10,000-flight summer schedule dataset.

**Approach:**
- Explored the flight schedule dataset (10,000 flights) covering route, region, haul type, time of day, aircraft type, and seat configuration
- Tested multiple grouping strategies (Haul + Time of Day, Haul + Region, Haul + Aircraft Type) to identify which best explained variation in lounge eligibility
- Selected **Haul Type + Time of Day** as the final model — it captured meaningful variation while remaining simple and always knowable at the schedule-planning stage
- Built a reusable **Category → Tier 1/2/3 %** lookup table and applied it to a sample of individual flights to estimate lounge demand
- Documented assumptions, methodology, and limitations in a written justification

**Deliverable:** `Task1_Lounge_Eligibility_Lookup_Table.xlsx`

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
- `Task2_Booking_Prediction_Model.ipynb`
- `Task2_Summary_Slide.pptx`

**Tools:** Python (pandas, scikit-learn, matplotlib/seaborn)

---

## 🛠️ Repository Structure

```
├── task1-lounge-eligibility/
│   └── Task1_Lounge_Eligibility_Lookup_Table.xlsx
├── task2-booking-prediction/
│   ├── Task2_Booking_Prediction_Model.ipynb
│   └── Task2_Summary_Slide.pptx
└── README.md
```

---

## 🎓 About

Completed as part of the **British Airways Data Science Job Simulation** on [Forage](https://www.theforage.com/).
