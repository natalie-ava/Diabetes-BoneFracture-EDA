# Results and Conclusions

This folder contains evaluation outputs and performance summaries from the predictive models developed. Two machine learning models, logistic regression and random forest, were tested to assess their ability to predict fracture risk using clinical and demographic data.

## Model Performance Summary

### Logistic Regression

- **Accuracy:** 90%  
- **Precision (Fracture Class):** 0.00  
- **Recall (Fracture Class):** 0.00  
- **F1-Score (Fracture Class):** 0.00  

<p align="center">
  <img src="https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/results/LR_confusion_matrix.png" width="600">
</p>

The logistic regression model correctly classified all non-fracture cases but failed to identify any fractures. While the model's accuracy appears high, this is misleading due to the complete absence of sensitivity. The model defaulted to predicting the majority class, triggering undefined precision warnings for the minority class (fractures).

### Random Forest (Baseline)

- **Accuracy:** 89%  
- **Precision (Fracture Class):** 0.00  
- **Recall (Fracture Class):** 0.00  
- **F1-Score (Fracture Class):** 0.00  

<p align="center">
  <img src="https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/results/RF_confusion_matrix.png" width="600">
</p>

The random forest model correctly classified nearly all non-fracture cases but failed to identify any fractures. While the model's overall accuracy appears strong, this is misleading due to the complete lack of recall for the minority class. Like the logistic model, it defaulted to predicting the majority class, resulting in zero sensitivity and undefined precision for fracture cases.

## Included Files

- [classification_report_logreg.txt](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/results/classification_report_logreg.txt) — Evaluation metrics for the logistic regression model  
- [classification_report_rf.txt](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/results/classification_report_rf.txt) — Evaluation metrics for the random forest model  
- [LR_confusion_matrix.png](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/results/LR_confusion_matrix.png) — Confusion matrix visualization for logistic regression  
- [RF_confusion_matrix.png](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/results/RF_confusion_matrix.png) — Confusion matrix visualization for random forest  
- [model_summary_notes.txt](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/results/model_summary_notes.txt) — Summary of findings and model comparison notes
---

## Conclusions

- Both models performed well on the majority class (non-fractures) but failed to identify fracture cases entirely.
- High accuracy does not reflect true model performance due to class imbalance.
- Future work should focus on improving model sensitivity using:
  - Resampling techniques
  - Feature expansion and interaction terms
  - Alternative modeling approaches (e.g., XGBoost, ensemble methods)

---

## Research Status

These results are part of an ongoing research and learning process. They are exploratory and subject to change as additional techniques are applied. Outputs in this folder should be interpreted as preliminary rather than final conclusions.
