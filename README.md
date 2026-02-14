# skygeni-sales-intelligence-challenge
# Skygeni Sales Intelligence Challenge
# AI-Driven Sales Intelligence System

## Overview

This project builds a lightweight Sales Intelligence system for B2B SaaS companies.  
The goal is to help CROs understand:

- Why win rate is changing
- Which factors are hurting or improving conversion
- What actions can improve revenue outcomes

The solution focuses on interpretability, business alignment, and practical decision intelligence rather than complex black-box modeling.

---

## 1. Problem Statement

The CRO observed a decline in win rate despite healthy pipeline volume.  
The objective was to:

- Diagnose drivers of win rate deterioration
- Quantify structural conversion factors
- Design a lightweight alert system for ongoing monitoring

---

## 2. Approach Overview

The solution is structured into:

1. Problem framing
2. Exploratory Data Analysis (EDA)
3. Win Rate Driver Modeling (Logistic Regression)
4. Sales Insight & Alert System Design
5. Reflection & Production Considerations

The modeling objective was not maximizing accuracy, but identifying interpretable drivers.

---

## 3. Data Exploration & Key Insights

Key findings from EDA:

- Win rate fluctuations are influenced more by stage progression than by product type alone.
- Certain industries (e.g., FinTech) show structurally higher win likelihood.
- Longer sales cycles negatively impact conversion.
- Lead source quality varies in effectiveness.

Custom metrics designed:
- Stage Loss Share
- Segment Impact Score
- 
These metrics helped isolate operational bottlenecks and segment-level performance shifts.

---

## 4. Decision Engine – Win Rate Driver Analysis

### Modeling Choice

A logistic regression model was implemented to:

- Estimate win probability
- Quantify the independent impact of deal characteristics
- Provide interpretable odds ratios

Why logistic regression?
- Transparent coefficients
- Directional interpretability
- Business-friendly explanation
- Avoids black-box complexity

### Key Drivers Identified

Strongest Negative Drivers:
- Qualified Stage
- Proposal Stage
- Partner Lead Source
- Longer Sales Cycles

Strongest Positive Drivers:
- FinTech Industry
- India Region
- Larger Deal Size

The results suggest process execution and deal progression are stronger drivers than pure segment characteristics.

---

## 5. Mini System Design

A lightweight Sales Insight & Alert System was proposed:

**Architecture:**
CRM → Data Warehouse → Feature Pipeline → Logistic Model → Insight Engine → Dashboard/Alerts

**Outputs:**
- Segment risk ranking
- Win probability per deal
- Stage-based deterioration alerts
- Sales cycle risk detection

**Execution Frequency:**
- Data ingestion: Daily
- Model retraining: Monthly/Quarterly
- Alerts: Weekly

---

## 6. Key Decisions & Tradeoffs

- Prioritized interpretability over model complexity
- Used logistic regression instead of tree-based models
- Avoided overfitting and heavy hyperparameter tuning
- Focused on decision intelligence, not Kaggle-style accuracy

Limitations:
- No rep-level data included
- Correlation, not causation
- Dependent on CRM data quality

---

## 7. How to Run the Project

### 1. Clone the repository

### 2. Run the Jupyter Notebook
