# Results and Conclusions

This folder contains evaluation outputs and performance summaries from the predictive models developed. Two machine learning models, logistic regression and random forest, were tested to assess their ability to predict fracture risk using clinical and demographic data.

## Model Performance Summary

### Logistic Regression

- **Accuracy:** 90%  
- **Recall (Fracture Class):** 0.00
  
**Confusion Matrix:**
  
|               | Predicted: No Fracture | Predicted: Fracture |
|---------------|--------------|--------------|
| Actual: No Fracture     | 455          | 0            |
| Actual: Fracture     | 51           | 0            |

-  The model classified all fracture cases incorrectly as non-fractures, despite correctly identifying all non-fracture cases. This reflects perfect specificity but zero sensitivity.

### Random Forest (Baseline)

- **Accuracy:** 89%  
- **Recall (Fracture Class):** 0.00
  
**Confusion Matrix:**
  
|               | Predicted: No Fracture | Predicted: Fracture |
|---------------|--------------|--------------|
| Actual: No Fracture     | 452          | 1            |
| Actual: Fracture     | 53           | 0            |

Like logistic regression, the random forest model failed to detect any fracture cases. It produced one false positive prediction for a non-fracture case.

---

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
