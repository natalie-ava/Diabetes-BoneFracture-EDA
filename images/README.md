# Data Visualizations

This folder contains the full set of visualizations generated during the exploratory and modeling phases of the project. These charts illustrate trends in age, race, lab values, and fracture prevalence and support the conclusions presented in the notebook and final report.

---

### [Target Population Ages](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/target_pop_age_dist.png)
<p align="center">
  <img src="https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/target_pop_age_dist.png" width="500">
</p>

This age distribution confirms that most participants fall between 65 and 75 years old, with the highest concentration near age 69. The population skews slightly younger within the 60+ range, which may influence fracture and lab trends. Age-based risk stratification could help tailor model interpretation.

---

### [Distribution of Race](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/race_dist.png)
<p align="center">
  <img src="https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/race_dist.png" width="500">
</p>

White and Hispanic men make up over 80% of the sample. This racial makeup reflects regional demographics in San Antonio and has implications for public health outreach. Models built on this data may not generalize well to areas with different racial compositions.

---

### [Fracture Rate by Diabetes and Age Group](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/diabetics_vs_fractures.png)
<p align="center">
  <img src="https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/diabetics_vs_fractures.png" width="500">
</p>

Fracture rates are consistently higher in individuals over 70, especially among diabetics. This supports the hypothesis that both age and diabetes increase fracture risk. However, the overlap between variables suggests models must account for interaction effects.

---

### [Prevalence of Fractures Among Diabetic Population](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/diabetics_fractures.png)
<p align="center">
  <img src="https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/diabetics_fractures.png" width="500">
</p>

Only a small fraction of diabetic men experienced fractures. This class imbalance presents a major modeling challenge, as most classifiers will default to predicting the majority class. Techniques like oversampling or weighted loss functions are needed.

---

### [Correlation Matrix](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/corr_matrix.png)
<p align="center">
  <img src="https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/corr_matrix.png" width="500">
</p>

There is no strong correlation between the selected lab values and age. This suggests the need for more complex relationships (e.g., nonlinear patterns or interactions) to be captured through modeling. It also supports the choice to include all three features in modeling.

---

### [Calcium Levels by Age and Diabetes Status](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/agecalc_diabetes.png)
<p align="center">
  <img src="https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/agecalc_diabetes.png" width="500">
</p>

This plot shows a fairly uniform spread of calcium values across ages, with no major visual difference between diabetic and non-diabetic men. This lack of separation weakens calcium’s individual predictive power, though it may still be valuable in combination with other features.

---

### [A1C Value Distribution by Age Group](https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/A1C_violinplot.png)
<p align="center">
  <img src="https://github.com/natalie-ava/Diabetes-BoneFracture-EDA/blob/main/images/A1C_violinplot.png" width="500">
</p>

Younger individuals (under 70) show greater variation in A1C values, while older individuals tend to cluster more tightly. This might reflect tighter glycemic control in older patients or survivor bias. It highlights age as a moderating variable in interpreting lab values.

---
