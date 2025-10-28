# Employee Communication Analysis and Engagement Risk Prediction

## Overview
This project analyzes employee communication (emails) to measure sentiment, engagement, and flight risk using **Python**, **TextBlob**, and **Scikit-learn**.  
It includes sentiment scoring, EDA, employee ranking, and a predictive model for engagement risk.

---

## Methodology
- **Data Source:** `test.csv` containing Subject, Body, Date, and Sender.  
- **Sentiment Labeling:** Using TextBlob polarity:  
  - Positive (> 0.1): +1  
  - Negative (< -0.1): -1  
  - Neutral (−0.1 to 0.1): 0  

A monthly sentiment score was calculated for each employee to identify top performers and potential risk profiles.

---

## Key Findings
| Sentiment | Share | Notes |
|------------|--------|-------|
| Neutral | **46.5%** | Objective communication |
| Positive | **44.6%** | High affirmation tone |
| Negative | **8.9%** | Low, but relevant for risk |

- Positive messages ≈ 326 chars (longest)  
- Negative messages ≈ 172 chars (shortest)  
- **6 employees** flagged under risk (≥4 negative messages in 30 days)  
- **Linear Regression Model:** R² = **0.67**

---

## How to Run
### Install Dependencies
- pip install pandas numpy scikit-learn matplotlib seaborn textblob
- python -m textblob.download_corpora

---

## Outputs
### File	Description
- top_positive_employees.csv	Top 3 positive employees
- top_negative_employees.csv	Top 3 negative employees
- flight_risk_employees.csv	Employees meeting 30-day risk threshold
- .png files	Sentiment distribution, trends, and model validation

--- 

## Tech Stack
Python • Pandas • NumPy • Matplotlib • Seaborn • Scikit-learn • TextBlob

