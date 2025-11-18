# AI Adoption & AI/ML Job Growth Prediction (Stack Overflow 2025)

**Author:** Jeremy Freeman  
**Course:** CSC 423 – Data Mining Research Project  
**Institution:** California Baptist University  


## Overview

This project analyzes how artificial intelligence is reshaping the software development workforce. Using the 2025 Stack Overflow Developer Survey, this study builds predictive models to:

- Predict the likelihood that a developer uses AI tools  
- Forecast the growth of AI/ML job roles over the next decade  
- Examine how developer salary correlates with AI adoption  

The project includes a complete data-mining pipeline, predictive models, and three final visualizations.


## Research Questions

1. What factors influence a developer’s likelihood of adopting AI tools?  
2. How will AI/ML roles change over the next 10 years?  
3. How is AI adoption related to developer salary and experience?  


## Dataset

**Source:** Stack Overflow Developer Survey 2025  
**File:** `survey_results_public.csv`  
**Rows:** ~49,000 respondents  

**Key fields used include:**

- `AISelect` – AI tool usage  
- `WorkExp` – years of experience  
- `ConvertedCompYearly` – annual compensation  
- `DevType` – job role  
- `EdLevel`, `Country`, and more  


## Methodology

### 1. Data Cleaning
- Removed incomplete and invalid entries  
- Filtered realistic ranges for salary and experience  
- Encoded categorical attributes  
- Selected data relevant to AI and job roles  

### 2. AI Adoption Prediction
A Random Forest classifier predicts a developer’s likelihood of using AI tools.  
The model outputs a continuous probability score:


### 3. AI/ML Role Forecasting
AI/ML-related developers were identified through the `DevType` field.  
A second Random Forest model predicts the growth of AI/ML roles.  
A logistic S-curve models the 10-year forecast (2025–2035).

### 4. Salary and AI Usage Relationship
A hexbin density plot visualizes how predicted AI adoption probability relates to compensation.  


## Visualizations

### Graph 1 — AI Adoption by Experience Level
Predicted AI adoption increases with developer experience.  
Includes 2025 survey statistic: **84%** of developers use or plan to use AI tools.

### Graph 2 — AI/ML Role Forecast (2025–2035)
Logistic S-curve projects AI/ML roles growing from ~2% to ~10–12% over the next decade.

### Graph 3 — Salary vs AI Usage (Hexbin Plot)
Higher predicted AI usage correlates with higher annual compensation.  


## Key Findings

- AI tool usage is widely adopted in the developer community.  
- Experience strongly correlates with AI adoption.  
- AI/ML job roles will likely continue expanding through 2035.  
- Higher compensation is associated with higher AI engagement.  


## How to Run

1. Open the notebook (`AI_Adoption_Forecast.ipynb`) in Google Colab.  
2. Place `survey_results_public.csv` into your Google Drive:  

