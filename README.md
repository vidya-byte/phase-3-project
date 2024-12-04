### Predicting Customer Churn for SyriaTel: Identifying Key Factors and Reducing Attrition
### Business Understanding
The data for this project was obtained from Kaggle. The primary stakeholders for this project include the marketing and customer service teams at SyriaTel, as well as senior management. SyriaTel, is a prominent telecommunications company, that faces significant revenue losses due to customer churn. This project aims to build a predictive model to identify customers at risk of churning by analyzing various features such as customer demographics, usage patterns, and billing information. By understanding the key factors influencing churn and predicting which customers are likely to leave, SyriaTel can implement targeted retention strategies, improve customer satisfaction, and ultimately enhance business sustainability. This approach not only helps in retaining valuable customers but also optimizes marketing efforts and reduces the costs associated with customer acquisition.

### Problem Statement:
SyriaTel faces significant revenue losses due to high customer churn. This project aims to develop a predictive model to identify at-risk customers and implement effective retention strategies.

### Business Objectives
Based on the problem statement, SyriaTel company has to set some objectives in order to curb the problem of customer churning. These are the objectives that will be resolved after creating a model that will address the business churning problem:

To identify the primary factors influencing customer churn at SyriaTel.

To determine whether predictive model can accurately identify customers who are likely to churn.

To determine whether the insights gained from the churn prediction model be used to enhance customer retention strategies.

To identify what business processes or interventions can be implemented based on the churn predictions to reduce customer attrition.

### Data Understanding
The dataset for this analysis includes features related to customer demographics, usage patterns, and billing information. Key features include the state of residence, length of account, area code, international plan, voice mail plan, total minutes and charges for calls made during the day, evening, and night, as well as the number of customer service calls. The target variable, churn, indicates whether a customer has left the service. This data provides a comprehensive overview of customer interactions, helping to identify patterns and factors that contribute to churn, enabling effective predictive modeling.

### Data Preparation 
Data Preparation involves transforming raw data into a suitable format for analysis. This step includes data cleaning, handling missing values, encoding categorical variables, normalizing numerical features, handling outliers, and creating new features through feature engineering. Proper data preparation ensures that the dataset is consistent and ready for the modeling phase, improving the performance and accuracy of the models.

### Exploratory Data Analysis (EDA)
This is a crucial step in the data science process that involves systematically exploring and summarizing the major features of a dataset. This includes summarizing the data, visualizing distributions, identifying patterns and relationships, and detecting anomalies or outliers. EDA helps in gaining insights into the data, guiding feature selection, and informing subsequent data preparation and modeling steps. Common techniques i used here include histograms, bar plots, scatter plots, box plots, and correlation heatmaps.The aim here is to gain a deeper understanding of the data, identify patterns, relationships and anomalies.
### Modelling

### EValuation

### Conclusion

### Recommendations







### Modelling
Accuracy:

The model achieved an accuracy of 0.856, meaning it correctly predicted 85.6% of the test samples. While this seems high, accuracy alone can be misleading, especially with imbalanced datasets.

Precision, Recall, and F1-Score:

For the majority class (False):
Precision: 0.86 (When the model predicts "not churn," it's correct 86% of the time).
Recall: 1.00 (The model correctly identifies 100% of the true "not churn" cases).
F1-Score: 0.92 (The harmonic mean of precision and recall, showing overall performance for this class).

For the minority class (True):
Precision: 1.00 (When the model predicts "churn," it's correct 100% of the time, though this is not meaningful given recall).
Recall: 0.01 (The model correctly identifies only 1% of the true "churn" cases, indicating poor performance in identifying churn).
F1-Score: 0.01 (Very low, reflecting poor performance for this class).

Confusion Matrix:

The confusion matrix shows:
True Negatives (TN): 855 (correctly predicted as "not churn").
False Positives (FP): 0 (incorrectly predicted as "churn").
False Negatives (FN): 144 (incorrectly predicted as "not churn").
True Positives (TP): 1 (correctly predicted as "churn").

Macro Average:
Precision: 0.93
Recall: 0.50
F1-Score: 0.47 These metrics average precision, recall, and F1-score across both classes, showing the disparity in model performance.

Weighted Average:
Precision: 0.88
Recall: 0.86
F1-Score: 0.79 These metrics consider the support (number of true instances for each class), providing a balanced view of performance.

### Decision Trees 
Accuracy:
The model achieved an accuracy of 0.93, meaning it correctly predicted 93% of the test samples.
Precision, Recall, and F1-Score:
For the majority class (False):
Precision: 0.94 (When the model predicts "not churn," it's correct 94% of the time).
Recall: 0.98 (The model correctly identifies 98% of the true "not churn" cases).
F1-Score: 0.96 (The harmonic mean of precision and recall, showing strong overall performance).
For the minority class (True):
Precision: 0.83 (When the model predicts "churn," it's correct 83% of the time).
Recall: 0.66 (The model correctly identifies 66% of the true "churn" cases).
F1-Score: 0.73 (Indicating reasonable performance for this class).
Confusion Matrix:
The confusion matrix shows:
True Negatives (TN): 835 (correctly predicted as "not churn").
False Positives (FP): 20 (incorrectly predicted as "churn").
False Negatives (FN): 50 (incorrectly predicted as "not churn").
True Positives (TP): 95 (correctly predicted as "churn").

Macro Average:
Precision: 0.88
Recall: 0.82
F1-Score: 0.85 These metrics average precision, recall, and F1-score across both classes.

Weighted Average:
Precision: 0.93
Recall: 0.93
F1-Score: 0.93 These metrics consider the support (number of true instances for each class), providing a balanced view of performance.

### Random Forest Results:
Accuracy:
The model achieved an accuracy of 0.889, correctly predicting 88.9% of the test samples.
Precision, Recall, and F1-Score:
For the majority class (False):
Precision: 0.89 (When the model predicts "not churn," it's correct 89% of the time).
Recall: 1.00 (The model correctly identifies 100% of the true "not churn" cases).
F1-Score: 0.94 (The harmonic mean of precision and recall, showing strong overall performance).
For the minority class (True):
Precision: 0.95 (When the model predicts "churn," it's correct 95% of the time).
Recall: 0.25 (The model correctly identifies only 25% of the true "churn" cases).
F1-Score: 0.39 (Indicating the model struggles with this class).

Confusion Matrix:
The confusion matrix shows:
True Negatives (TN): 853 (correctly predicted as "not churn").
False Positives (FP): 2 (incorrectly predicted as "churn").
False Negatives (FN): 109 (incorrectly predicted as "not churn").
True Positives (TP): 36 (correctly predicted as "churn").
Macro and Weighted Averages:
Macro Average: Averages the performance metrics across classes, indicating that while precision is high (0.92), recall is low (0.62), leading to moderate F1-score (0.67).
Weighted Average: Accounts for the number of instances in each class, showing that the model performs well overall (0.90 precision, 0.89 recall, 0.86 F1-score) but highlights the imbalance in predicting churn.
=======

>>>>>>> origin/main
