# Tree-Based-Algorithms-on-loan-data
Loan Dataset Analysis and Classification
Exploratory Data Analysis (EDA)
Applied Label Encoding to categorical features.

Heatmap Analysis showed no significant correlation affecting the target variable.

Observed that the data does not follow a normal distribution.

Feature Scaling
Used MinMaxScaler to scale input features between 0 and 1.

Model 1: Gradient Boosting Classifier (Imbalanced Data)
Initial classification results showed:

Class 0 (majority class) had good precision and recall.

Class 1 (minority class) had an F1-score of 0.00 because:
1️⃣ Recall for Class 1 = 0.00 → The model never correctly predicted Class 1.
2️⃣ Precision for Class 1 = 0.68, but with recall 0, the F1-score remained 0.

Conclusion: The model completely failed to detect Class 1.

Balancing Data with SMOTE
Used SMOTE (Synthetic Minority Over-sampling Technique) to handle class imbalance.

Applied RandomForestClassifier after balancing the dataset.

Results:

F1-score improved significantly.

Accuracy increased to 90%.

RandomForestClassifier performed better than Gradient Boosting after handling imbalance.

Loan Risk Prediction
Implemented RandomForestClassifier, which provided the best results compared to Gradient Boosting.

Car Ownership Prediction (Using Same Data)
Compared multiple models:

Gradient Boosting Classifier achieved the best accuracy (74.5%), outperforming Logistic Regression.

House Ownership Prediction
Followed the same pipeline for predicting House Ownership.

Class imbalance affected the confusion matrix.

Used Decision Tree with hyperparameter tuning.

Achieved 95% accuracy, demonstrating a strong predictive performance.
