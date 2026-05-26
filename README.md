# Personal Loan Acceptance Prediction
Developers Hub Corporation | Internship Task 5

## Overview

Banks spend significant resources on marketing campaigns, calling thousands of customers to offer personal loan products. Most of those calls go nowhere. This project builds a machine learning pipeline to predict which customers are actually likely to say yes, so that marketing efforts can be directed where they matter.

The dataset comes from a real Portuguese bank's direct marketing campaign, containing over 45,000 customer records with demographic information, account details, and campaign interaction history. The target variable is whether the customer accepted the loan offer.

## Dataset

Bank Marketing Dataset, sourced from the UCI Machine Learning Repository via Kaggle.

- 45,211 customer records across 17 features
- Target variable: deposit (yes/no) indicating loan acceptance
- Key features: age, job, marital status, education, account balance, call duration, campaign contacts, and previous outcome

The dataset is heavily imbalanced. Roughly 88% of customers did not accept the offer, which makes this a realistic and challenging classification problem.

## What Was Done

### Data Cleaning and Preparation
- Checked for missing values and duplicate records
- Applied Label Encoding to all categorical variables
- Split data into 80% training and 20% test sets using stratified sampling to preserve class balance

### Exploratory Data Analysis
Seven visualizations were built to understand the data before modeling: a class balance chart, age distribution by acceptance, acceptance rate by job type, marital status breakdown, education level comparison, a box plot of call duration versus acceptance, and a full correlation heatmap.

### Model Training
- Logistic Regression (max_iter=1000, random_state=42)
- Decision Tree Classifier (max_depth=5, random_state=42)

### Evaluation
Accuracy scores, classification reports, and confusion matrices were generated for both models alongside a feature importance plot and acceptance rate breakdowns by age group, job, and marital status.

## Results

| Model | Accuracy |
|-------|----------|
| Logistic Regression | 78.59% |
| Decision Tree | 80.70% |

The Decision Tree outperformed Logistic Regression on accuracy and also provided interpretable feature importance scores, making it the more useful model for deriving business insights.

## Key Findings

- Call duration is the strongest predictor of acceptance. Customers who stayed on the call longer were significantly more likely to say yes.
- Students and retired customers had the highest acceptance rates by job category.
- Single customers accepted at slightly higher rates than married ones.
- Younger customers (18 to 30) and older customers (60+) were more receptive than the middle age groups.
- Customers with a positive outcome from a previous campaign were far more likely to accept again.

## Business Recommendation

If this model were deployed, the bank could pre screen its customer list before running a campaign and focus calls on the high probability segments identified here. Targeting single, younger or retired customers with a history of positive campaign engagement, and training call agents to extend conversation length, would likely improve conversion rates and reduce cost per acquisition.

## Tech Stack

- Python 3
- pandas, NumPy
- matplotlib, seaborn
- scikit-learn (LogisticRegression, DecisionTreeClassifier, LabelEncoder, train_test_split)


## Author

Aiman Ishaq
CS Student, ACE College | Data Analyst Intern, Developers Hub Corporation

GitHub: github.com/aiman-ami
LinkedIn: linkedin.com/in/aiman-ishaq
