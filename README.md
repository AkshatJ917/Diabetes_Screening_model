🩺 **Diabetes Screening Prediction using Machine Learning**
📌 **Overview**

This project builds a machine learning model to predict diabetes risk with a strong focus on minimizing false negatives. Since this is a screening problem, identifying potential diabetic patients (high recall) is more critical than maximizing overall accuracy.

After comparing multiple models, the final selected model is Gradient Boosting with a decision threshold of 0.26.

🔍 **Models Evaluated**:
Logistic Regression
Decision Tree
Random Forest
Gradient Boosting

🔍**Models were evaluated using:**
Accuracy
Precision
Recall
F1-Score
ROC-AUC
Cross-validation score

✅ **Why Gradient Boosting?**

Gradient Boosting was chosen because:
->It showed more stable and consistent cross-validation performance compared to Random Forest.
->It achieved strong ROC-AUC (~0.83).
->It maintained balanced performance across evaluation metrics.
->Although Random Forest performed competitively, Gradient Boosting generalized more reliably.

⚙️ **Hyperparameter Tuning & Threshold Optimization**

Grid Search was applied to optimize the model. However:
->The tuned model required lowering the threshold to 0.10 to achieve a recall of 0.79.
->This was still lower than the 0.85 recall achieved by the original model at threshold 0.26.
Since minimizing false negatives is the primary objective, threshold optimization proved more effective than further hyperparameter tuning.

📊 **Final Model Performance (Threshold = 0.26)**

Recall (Class 1): 0.85
Precision: 0.62
Accuracy: 0.77
ROC-AUC: ~0.83
False Negatives: 8
This configuration significantly reduces missed diabetic cases while maintaining balanced overall performance.


