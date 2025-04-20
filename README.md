# Predicting E-Commerce Order Cancellations
Mini-project FR1-Group 8

## Introduction & Motivation
This is a repository for SC1015: Intro to Data Science & Artifical Intelligence Mini-project. We aim to predict e-commerce order cancellations using real transaction data from Amazon.in.

Even small cancellation rates can cause lost revenue, wasted logistics, and customer dissatisfaction.
By identifying high-risk orders early, platforms can take action to reduce cancellations and improve efficiency. We explore if a data-driven approach can help address this issue at scale.

## Problem Statement
- Can we use order-level data to predict order cancellations and reduce revenue loss?
- Which model would be the best to predict it?

## Dataset & Preparation
- Source: Kaggle – [E-Commerce Sales Dataset],  ~129,000 transaction
- Removed irrelevant columns
- Handled missing values
- Filtered dataset
- Encoded categorical variables numerically
- Added readable category labels via Category_name

## EDA
- About 14.45% of orders are cancelled → class imbalance
- Merchant-fulfilled orders are ~45% more likely to be cancelled
- No promotion orders have a high cancellation rate (~36.7%)
- Cancelled orders tend to be lower in value
- Set and Kurta are both high-volume and high-cancellation categories

## Machine Learning Models
#### Models Used:
- Logistic Regression (Baseline)
- Random Forest & Random Forest(Balanced)
- XGBoost

#### Evaluation Metrics:
- Accuracy
- True Negative Rate, True Positive Rate(Recall)
- Confusion Matrix

## What We Learned
- Logistic Regression is a good baseline — simple but effective
- Random Forest performed best overall, even without tuning
- XGBoost didn’t outperform — complexity ≠ better
- Accuracy alone isn’t enough — recall matters for imbalanced data
- Tuning (threshold + class weights) improves recall

## Conclusion & Recommendations
- High order amount → fewer cancellations
- Merchant fulfillment → more cancellations
- Promotions help reduce cancellations
- Using random forest ML model to flag high-risk orders early
- Improving merchant fulfillment speed
- Offering targeted promotions for risky categories

## Contributors
- @ani-i25 Gao Anni (N2402461C): Data cleaning, EDA, GitHub setup
- @Chenyu-Alex Liu Chenyu (N2402421L): ML modeling, performance tuning, insights, video editing

## References
- Kaggle Dataset: https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data/data
- Classification in Machine Learning: https://www.datacamp.com/blog/classification-machine-learning
- Scikit-learn RandomForestClassifier: https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html
- Scikit-learn XGBoost: https://scikit-learn.org/stable/modules/ensemble.html
- Analysis on E-commerce Order Cancellations Using Market Segmentation Approach: https://dl.acm.org/doi/fullHtml/10.1145/3450588.3450596
- Seaborn Color Palette: https://seaborn.pydata.org/tutorial/color_palettes.html
