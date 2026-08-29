# British Airways Data Science Job Simulation (Forage)

[![Python 3.12.6](https://img.shields.io/badge/Python-3.12.6-e34fc3?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/) 
[![Vite](https://img.shields.io/badge/Vite-Frontend-orange?style=for-the-badge&logo=vite&logoColor=white)](https://vite.dev/) 
[![javascript](https://img.shields.io/badge/JavaScript-ded416?style=for-the-badge&logo=JavaScript&logoColor=white)]([https://vite.dev/](https://developer.mozilla.org/de/docs/Web/JavaScript)) 
[![FastAPI](https://img.shields.io/badge/FastAPI-Backend-24bf2c?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) 

<!--![Status](https://img.shields.io/badge/status-in--progress-yellow)-->
![License](https://img.shields.io/badge/license-MIT-green)
![scikit-learn](https://img.shields.io/badge/sklearn-ML-orange)
![OSMnx](https://img.shields.io/badge/OSMnx-network--data-lightgrey)
[![RoA](https://img.shields.io/badge/RoA%20-Springer-3636cf?style=for-the-badge&logo=springer&logoColor=white)](https://link.springer.com/chapter/10.1007/978-3-031-56826-8_10)

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
    ├── Task 1 Modeling lounge eligibility at Heathrow Terminal 3/
    │   └── British Airways Summer Schedule Dataset - Forage Data Science Task 1.xlsx (Task analysis)
    |   └── Lounge Eligibility Lookup Template - Task 1.xlsx (Final Submission)
    └── Task2/
        ├── 2. Predicting customer buying behaviour.docx
        └── Getting Started.ipynb
└── README.md
```

---

## 🎓 About

Completed as part of the **British Airways Data Science Job Simulation** on [Forage](https://www.theforage.com/).
