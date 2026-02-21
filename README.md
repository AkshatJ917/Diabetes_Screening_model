# 🩺 Diabetes Screening Prediction (Machine Learning Project)

## 📌 Project Objective

This project builds a machine learning model to predict diabetes risk with a strong focus on minimizing false negatives. Since this is a medical screening problem, identifying potential diabetic patients (high recall) is more important than maximizing overall accuracy.

---

## 🔎 Models Evaluated

- Logistic Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting  

Models were evaluated using:
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- ROC-AUC  
- Cross-validation score  

---

## ✅ Why Gradient Boosting?

Gradient Boosting was selected because:

- It showed more stable and consistent cross-validation performance compared to Random Forest  
- It achieved strong ROC-AUC (~0.83)  
- It demonstrated reliable generalization across folds  

Although Random Forest performed competitively, Gradient Boosting proved to be more stable overall.

---

## ⚙️ Hyperparameter Tuning vs Threshold Optimization

Grid Search was applied to tune the Gradient Boosting model.

However:
- Even after tuning, lowering the threshold to 0.10 resulted in a recall of 0.79  
- The original model with a threshold of 0.26 achieved a higher recall of 0.85  

Since minimizing false negatives is the primary objective, threshold optimization was more effective than additional hyperparameter tuning.

---

## 📊 Final Model Performance (Threshold = 0.26)

- Recall (Diabetes Class): 0.85  
- Precision: 0.62  
- Accuracy: 0.77  
- ROC-AUC: ~0.83  
- False Negatives: 8  

This configuration significantly reduces missed diabetic cases while maintaining balanced overall performance.

---

## 🏆 Final Conclusion

The original Gradient Boosting model with threshold 0.26 was selected as the final model because it:

- Demonstrates stable cross-validation performance  
- Achieves the highest recall (0.85)  
- Minimizes false negatives  
- Maintains strong ROC-AUC and balanced precision  

The final model is both statistically sound and aligned with real-world medical screening priorities.
