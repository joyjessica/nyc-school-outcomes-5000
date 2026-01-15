# Breaking the Cycle: How School Quality and Socioeconomics Shape Student Outcomes

**Author:** Jessica Joy  
**Course:** DSAN 5000  
**Scope:** NYC Public High Schools (~500 schools)

## Overview

This project studies how **school quality and socioeconomic factors** influence three tightly linked student outcomes in NYC public high schools:

- Chronic absenteeism  
- High school dropout rates  
- College persistence (returning for year 2)

Using exploratory analysis, unsupervised learning, and supervised ML, I identify key drivers of risk and build models to **flag schools that would benefit most from early intervention**.

---

## Research Questions

- What school and socioeconomic factors most influence student outcomes?
- How are absenteeism, dropout, and college persistence connected?
- Can early academic indicators identify high-risk schools?

---

## Data

- ~500 NYC public high schools
- Sources: NYC DOE quality reports + socioeconomic indicators
- Features include:
  - Supportive environment & rigorous instruction scores
  - Grade 8 proficiency
  - Economic hardship indicators (temporary housing, ELL %, etc.)
  - Attendance, dropout, and college persistence

---

## Key Findings (EDA)

- Dropout rates are highest in the Bronx, especially Districts 12 and 8
- Schools with **lower household income** have significantly higher dropout rates
- Schools with **weaker supportive environments** have higher chronic absenteeism
- **Grade 8 proficiency strongly predicts college persistence**

---

## Methods

### Unsupervised Learning
- **PCA & t-SNE** reveal strong structure separating schools by outcomes
- **Agglomerative clustering** identifies a high-performing cluster with:
  - Low absenteeism
  - Low dropout
  - High college persistence

### Supervised Learning

**Regression (LASSO) – Chronic Absenteeism**
Top drivers:
- Supportive Environment Score (most important)
- Grade 8 Proficiency
- Rigorous Instruction Score
- % ELL, % Temporary Housing

**Binary Classification – Dropout Risk (Gradient Boosting)**
- Recall on high-risk schools: **91%**
- Key drivers: college persistence, temporary housing %, overage/undercredited %

**Multiclass Classification – College Persistence**
- Accuracy: **78%**
- Most important feature: **Grade 8 Proficiency**
- Absenteeism and dropout also strong predictors

---

## Key Takeaways

- **Grade 8 proficiency is a powerful early indicator of long-term success**
- **Supportive school environments reduce absenteeism**
- **Economic disadvantage strongly predicts dropout and low persistence**
- **Absenteeism, dropout, and college persistence form a connected risk pipeline**

## Why This Matters

This project shows how data science can help identify schools at risk early, enabling targeted, high-impact intervention before students fall off track.
