# Customer Churn Model Comparison

## Project Overview

Customer churn prediction is one of the most important applications of machine learning in business analytics. Companies can use predictive models to identify customers who are likely to leave and implement retention strategies before churn occurs.

This project develops and compares five machine learning classification models:

- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost
- LightGBM

The objective is to determine which model best predicts customer churn using the IBM Telco Customer Churn dataset.

---

## Business Problem

Customer acquisition is expensive.

Retaining existing customers is often significantly cheaper than acquiring new ones.

The goal of this project is to predict whether a customer will churn based on:

- Demographics
- Contract information
- Service subscriptions
- Billing information
- Customer tenure

---

## Dataset

### IBM Telco Customer Churn Dataset

Dataset Size:

```text
7043 rows × 21 columns
```

Target Variable:

```text
Churn
```

- Yes → Customer left
- No → Customer stayed

---

## Project Workflow

### 1. Data Understanding

- Dataset inspection
- Feature exploration
- Data types analysis

### 2. Data Cleaning

- Missing value analysis
- TotalCharges conversion
- CustomerID removal

### 3. Exploratory Data Analysis

Performed:

- Churn distribution analysis
- Contract type analysis
- Monthly charges analysis
- Customer tenure analysis

### Key Findings

#### Contract Type

Month-to-month customers showed significantly higher churn rates than customers with long-term contracts.

#### Tenure

Customers with shorter tenure were more likely to churn.

#### Monthly Charges

Higher monthly charges were associated with increased churn probability.

---

## Feature Engineering

### Encoding

Categorical variables were transformed using:

```python
pd.get_dummies()
```

Resulting Dataset:

```text
7043 rows × 31 columns
```

---

## Train-Test Split

```python
train_test_split(
    test_size=0.2,
    random_state=42
)
```

Training Set:

```text
5634 samples
```

Testing Set:

```text
1409 samples
```

---

## Models Implemented

### Decision Tree

```python
DecisionTreeClassifier()
```

### Random Forest

```python
RandomForestClassifier()
```

### Gradient Boosting

```python
GradientBoostingClassifier()
```

### XGBoost

```python
XGBClassifier()
```

### LightGBM

```python
LGBMClassifier()
```

---

## Model Performance

| Model | Accuracy | Precision | Recall | F1 Score |
|---------|---------|---------|---------|---------|
| Decision Tree | 0.7097 | 0.4519 | 0.4531 | 0.4525 |
| Random Forest | 0.7892 | 0.6429 | 0.4584 | 0.5352 |
| Gradient Boosting | 0.8091 | 0.6722 | 0.5442 | 0.6015 |
| XGBoost | 0.8133 | 0.6846 | 0.5469 | 0.6080 |
| LightGBM | 0.7984 | 0.6459 | 0.5282 | 0.5811 |

---

## Best Performing Model

### XGBoost

Performance:

| Metric | Score |
|---------|---------|
| Accuracy | 81.33% |
| Precision | 68.46% |
| Recall | 54.69% |
| F1 Score | 60.80% |

XGBoost achieved the highest overall performance and provided the best balance between precision and recall.

---

## Key Learnings

### Decision Tree

- Simple and interpretable
- Lowest performance

### Random Forest

- Reduced overfitting
- Improved predictive accuracy

### Gradient Boosting

- Sequential learning approach
- Significant performance improvement

### XGBoost

- Best overall model
- Highest F1 Score
- Industry-standard boosting algorithm

### LightGBM

- Fast and scalable
- Competitive performance

---

## Business Insights

Customers are more likely to churn when:

- They have month-to-month contracts
- They have shorter tenure
- They pay higher monthly charges
- They use electronic check payment methods

Customers are less likely to churn when:

- They have long-term contracts
- They have higher tenure
- They maintain long-standing relationships with the company

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- LightGBM
- Jupyter Notebook

---

## Machine Learning Concepts Demonstrated

- Classification
- Decision Trees
- Random Forests
- Gradient Boosting
- XGBoost
- LightGBM
- Feature Engineering
- One-Hot Encoding
- Model Evaluation
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Model Comparison

---

## Future Improvements

Potential enhancements:

- Hyperparameter Tuning
- GridSearchCV
- ROC-AUC Analysis
- Precision-Recall Curves
- Feature Selection
- Explainable AI (SHAP)

---

## Author

Stephen Mariga Ndegwa

AI Engineering & Machine Learning Portfolio Project

Focused on Machine Learning, Data Science, Predictive Analytics, and AI Systems Development.
