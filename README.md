# Predicting Bone Fractures in Diabetic Men Over 60

## Abstract
Part of a larger research effort, this project aims to predict bone fractures in diabetic men through exploratory data analysis and predictive modeling. The analysis is based on clinical and lifestyle data collected from a population of men over 60 in San Antonio,TX. Using logistic regression and random forest classifiers, the project explores how factors such as vitamin D levels, calcium levels, A1C, testosterone, smoking status, and insulin-use relate to fracture outcomes. Despite achieving high overall accuracy, both models fail to detect actual fracture cases due to class imbalance, highlighting the need for more robust approaches to improve predictive sensitivity.

## Project Overview
This project examines the relationship between diabetes, fracture prevalence, and bone health in a male population based in San Antonio, TX. It began as an exploratory data analysis focused on age- and race-based disparities and was later extended into a predictive modeling task. Multiple clinical datasets were merged and analyzed using Python to identify patterns and build models that predict the likelihood of a fracture based on key indicators such as vitamin D, calcium levels, A1C, testosterone, smoking status, and insulin use. The project demonstrates how EDA, statistical reasoning, and machine learning can be combined to support public health insights and risk prediction.

## Objectives
This project aims to:
- Clean and preprocess clinical data  
- Perform exploratory data analysis (EDA)  
- Visualize patterns and outcomes related to fracture status  
- Train and evaluate classification models (random forest and logistic regression)  
- Compare performance using confusion matrices, recall, and F1-score  
- Discuss clinical implications of the findings  

## Methods
- Filtered dataset to include diabetic men only  
- Selected six features: `Vit_D_val`, `calcium_val`, `A1C_value`, `testost_val`, `smoker_status`, and `on_insulins`  
- Dropped rows with missing values  
- One-hot encoded categorical variables  
- Trained logistic regression and random forest classifiers  
- Evaluated models using confusion matrices, precision, recall, and F1-score  

## Results

### Random Forest Classifier (Baseline Model)

**Confusion Matrix**

|               | Predicted: No Fracture (0) | Predicted: Fracture (1) |
|---------------|----------------------------|--------------------------|
| Actual: 0     | 452                        | 1                        |
| Actual: 1     | 53                         | 0                        |

**Classification Report**
```
           precision    recall  f1-score   support
       0       0.90      1.00      0.94       453
       1       0.00      0.00      0.00        53
accuracy                           0.89       506
```

### Logistic Regression (Comparison Model)

**Confusion Matrix**

|               | Predicted: No Fracture (0) | Predicted: Fracture (1) |
|---------------|----------------------------|--------------------------|
| Actual: 0     | 455                        | 0                        |
| Actual: 1     | 51                         | 0                        |

**Classification Report**
```
           precision    recall  f1-score   support
       0       0.90      1.00      0.95       455
       1       0.00      0.00      0.00        51
accuracy                           0.90       506
```
## Conclusion
Both models achieved strong overall accuracy but failed to detect fracture cases, misclassifying all positive outcomes. This outcome reflects the limitations of modeling rare health events in imbalanced datasets without adequate feature depth or class sensitivity.

## Recommendations
- Use oversampling methods to address class imbalance  
- Include additional features like bone density and fall history  
- Collaborate with Clinicians to interpret patterns and validate whether the model aligns with known fracture risk factors

## Ethical Considerations
This model is intended solely for educational and exploratory purposes and should not be used for clinical diagnosis or decision-making. Predictions may reflect biases in the underlying data and require further validation before real-world use.

## Repository Contents
- [`BoneFractureDataLab_Natalie.ipynb`](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/BoneFractureDataLab_Natalie.ipynb): Full notebook with data cleaning, EDA, modeling, and evaluation  
- `images/`: Folder for confusion matrices and plots  
- `results/`: Folder for saved model outputs  

## Technologies Used
- Python  
- pandas, NumPy  
- scikit-learn  
- matplotlib, seaborn  
