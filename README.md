# HR Analytics – Employee Attrition Prediction

## Project Overview

Employee attrition is one of the most significant challenges faced by organizations. High employee turnover leads to increased recruitment costs, training expenses, productivity loss, and disruption of business operations.

This project aims to leverage Machine Learning and Business Intelligence techniques to predict employee attrition, identify key drivers behind employee turnover, and provide actionable insights for HR teams through interactive Power BI dashboards.

---

# Business Problem

Organizations often struggle to identify employees who are likely to leave before resignation occurs.

Key challenges include:

* Increasing recruitment and onboarding costs
* Loss of experienced employees
* Reduced team productivity
* Difficulty in workforce planning

The objective of this project is to build a predictive model capable of identifying employees at risk of attrition and providing HR teams with actionable recommendations.

---

# Project Objectives

The project focuses on:

* Understanding employee attrition patterns
* Identifying factors influencing attrition
* Building predictive machine learning models
* Segmenting employees by attrition risk
* Creating interactive dashboards for HR decision-making

---

# Dataset Description

### Dataset

IBM HR Analytics Employee Attrition Dataset

### Dataset Size

* Total Employees: 1,470
* Features: 35
* Target Variable: Attrition

### Target Variable

| Value | Meaning         |
| ----- | --------------- |
| Yes   | Employee Left   |
| No    | Employee Stayed |

### Key Features

#### Employee Demographics

* Age
* Gender
* Marital Status
* Education
* Education Field

#### Job Information

* Department
* Job Role
* Job Level
* Monthly Income
* Business Travel

#### Employee Experience

* Total Working Years
* Years at Company
* Years in Current Role

#### Satisfaction Metrics

* Job Satisfaction
* Environment Satisfaction
* Work-Life Balance
* Relationship Satisfaction

#### Work Pattern

* Overtime
* Training Times Last Year

---

# Project Workflow

```text
Dataset
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Feature Engineering
   ↓
Data Preprocessing
   ↓
Machine Learning Models
   ↓
Model Evaluation
   ↓
Risk Prediction
   ↓
Power BI Dashboard
   ↓
Business Recommendations
```

---

# Step 1: Data Cleaning

The dataset was first inspected for:

* Missing values
* Duplicate records
* Incorrect data types
* Irrelevant columns

### Removed Columns

The following columns were removed because they provide no predictive value:

* EmployeeCount
* EmployeeNumber
* Over18
* StandardHours

### Why?

These columns contain constant values or unique identifiers that do not contribute to attrition prediction.

---

# Step 2: Exploratory Data Analysis (EDA)

EDA was performed to understand the relationship between employee attributes and attrition.

### Attrition Distribution

A count plot was used to visualize employee attrition.

Finding:

* Approximately 16% of employees had left the organization.

---

### Overtime Analysis

Attrition was compared against overtime status.

Finding:

* Employees working overtime showed significantly higher attrition rates.

---

### Department Analysis

Attrition was analyzed across departments.

Finding:

* Research & Development and Sales experienced the highest employee turnover.

---

### Job Role Analysis

Attrition was analyzed by job role.

Finding:

* Laboratory Technicians
* Sales Executives
* Research Scientists

showed higher attrition counts.

---

### Age Analysis

Employee age was compared with attrition.

Finding:

* Employees aged 26–35 exhibited higher attrition rates.

---

### Satisfaction Analysis

Job Satisfaction and Work-Life Balance were analyzed.

Finding:

* Lower satisfaction levels were associated with higher attrition.

---

# Step 3: Data Preprocessing

Before model training, the data was prepared.

### Target Variable Encoding

Attrition values were converted:

| Original | Encoded |
| -------- | ------- |
| Yes      | 1       |
| No       | 0       |

---

### Categorical Encoding

Categorical columns were transformed using One-Hot Encoding.

Examples:

* Gender_Male
* OverTime_Yes
* Department_Sales

---

### Feature Scaling

StandardScaler was used for Logistic Regression to normalize numerical features.

Benefits:

* Faster convergence
* Improved model performance

---

# Step 4: Machine Learning Models

Two classification algorithms were used.

---

## Logistic Regression

### Why Logistic Regression?

* Suitable for binary classification
* Easy to interpret
* Produces probability scores

### Model Training

The dataset was split:

* Training Set: 80%
* Testing Set: 20%

The Logistic Regression model was trained using Scikit-Learn.

### Results

* Accuracy: ~85%

---

## Decision Tree Classifier

### Why Decision Tree?

* Captures non-linear relationships
* Easy to visualize
* Provides feature importance

### Results

* Accuracy: ~82–85%

---

# Step 5: Model Evaluation

Several evaluation metrics were used.

### Accuracy

Measures overall prediction correctness.

### Confusion Matrix

Used to evaluate:

* True Positives
* True Negatives
* False Positives
* False Negatives

### Classification Report

Included:

* Precision
* Recall
* F1 Score

### ROC-AUC Score

Used to evaluate model discrimination capability.

---

# Step 6: Risk Prediction

Using Logistic Regression probabilities, a risk score was assigned to every employee.

### Risk Categories

| Probability | Category    |
| ----------- | ----------- |
| < 0.40      | Low Risk    |
| 0.40 – 0.70 | Medium Risk |
| > 0.70      | High Risk   |

This segmentation allows HR teams to prioritize retention efforts.

---

# Step 7: Power BI Dashboard Development

Four dashboard pages were created.

---

## Page 1: Executive Summary

### KPIs

* Total Employees
* Attrition Count
* Attrition Rate %
* Average Salary

### Visualizations

* Attrition by Department
* Attrition by Job Role
* Attrition by Gender

Purpose:

Provide a high-level overview of employee attrition.

---

## Page 2: Attrition Drivers

### Visualizations

* Overtime vs Attrition
* Job Satisfaction vs Attrition
* Work-Life Balance vs Attrition
* Monthly Income vs Attrition

Purpose:

Identify key factors contributing to employee turnover.

---

## Page 3: Demographics Dashboard

### Visualizations

* Age Group vs Attrition
* Gender vs Attrition
* Marital Status vs Attrition
* Education Field vs Attrition

Purpose:

Understand attrition patterns across employee demographics.

---

## Page 4: Prediction Dashboard

### KPIs

* Low Risk Employees
* Medium Risk Employees
* High Risk Employees
* Average Risk Score

### Visualizations

* Risk Category Distribution
* Department vs Risk Category
* Job Role vs Risk Category

Purpose:

Monitor employees at risk of leaving.

---

# Key Insights

### Insight 1

Employees working overtime are significantly more likely to leave.

### Insight 2

Research & Development and Sales departments show higher attrition counts.

### Insight 3

Laboratory Technicians and Sales Executives are among the most affected roles.

### Insight 4

Employees with lower monthly income demonstrate higher attrition risk.

### Insight 5

Most employees fall under the Low-Risk category, while a smaller group requires immediate HR attention.

---

# Recommendations

### Workforce Planning

Reduce excessive overtime through better staffing strategies.

### Employee Engagement

Conduct regular feedback and satisfaction surveys.

### Career Growth

Provide learning and promotion opportunities for younger employees.

### Retention Programs

Focus on employees identified as High Risk.

### Compensation Review

Evaluate salary structures for vulnerable employee groups.

---

# Project Outcome

* Successfully developed a machine learning-based employee attrition prediction system.
* Achieved approximately 85% predictive accuracy.
* Built interactive Power BI dashboards for HR stakeholders.
* Enabled proactive employee retention strategies through predictive analytics.

---

# Technologies Used

### Programming

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn

### Business Intelligence

* Power BI

### Machine Learning Models

* Logistic Regression
* Decision Tree Classifier

---

# Future Enhancements

* Random Forest Classifier
* XGBoost Model
* Real-Time Dashboard Integration
* Automated Risk Alerts
* Employee Retention Recommendation Engine
