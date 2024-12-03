<<<<<<< HEAD







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
