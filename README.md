# Insurance-Charges-Modeling

Predicting medical insurance charges using machine learning models to analyze the impact of demographic and health features, highlighting key factors such as smoking status, BMI, and age.

## Overview

The goal of this project is to predict individual medical insurance charges based on demographic and health-related features. The dataset includes age, sex, BMI, number of children, smoking status, and region. The project identifies the most significant factors affecting insurance costs and builds models to capture both linear and nonlinear relationships in the data.

## Dataset Details

**Title:** Medical Insurance Cost Dataset  
**Source:** [Kaggle](https://www.kaggle.com/datasets/mosapabdelghany/medical-insurance-cost-dataset)  
**Contents:** Information for 1,338 individuals including demographic and health-related features: age, sex, BMI, number of children, smoking status, and residential region in the US. The target variable is `charges`, representing medical insurance costs billed to the individual.  
 
## Project Workflow

### Data Collection and Preprocessing

- Loaded the dataset and converted categorical variables (`sex`, `smoker`) to numeric values.  
- One-hot encoded the `region` variable.  
- Standardized numerical features.  
- Checked for multicollinearity using Variance Inflation Factor (VIF).  
- Visualized feature distributions and ensured preprocessing correctness.  

### Exploratory Data Analysis (EDA)

- Plotted distributions of all features to identify skewness and outliers.  
- Created scatter plots of features versus charges to observe relationships.  
- Notable insights:  
  - Charges increase with age and BMI.  
  - Smokers consistently have higher insurance costs.  
  - Interactions, such as BMI × smoker, significantly impact charges.  

### Model Building and Evaluation

1. **Linear Regression**  
   - Baseline model to understand feature relationships.  
   - Evaluated using R², adjusted R², and residual plots.  
   - Identified age, BMI, and smoking status as significant predictors.  

2. **Polynomial Regression with Interaction Terms**  
   - Added pairwise feature interactions (e.g., BMI × smoker, age × smoker) to capture nonlinear effects.  
   - Improved R² and adjusted R² compared to linear regression.  
   - Visualized residuals to assess model improvements.  

3. **Gradient Boosting Regressor**  
   - Modeled complex nonlinear relationships and reduced residual errors.  
   - Achieved the highest predictive accuracy while maintaining generalization.  
   - Feature importance analysis confirmed smoker status, BMI, and age as dominant predictors.  

### Results

- Linear Regression: Test R² ≈ 0.79  
- Polynomial Regression: Test R² ≈ 0.87  
- Gradient Boosting: Test R² ≈ 0.89  

### Key insights:  
- Smoking status is the dominant factor driving insurance costs.  
- BMI and age also significantly influence charges, especially when combined with smoking.  
- Regional and demographic variables have smaller but interpretable effects.  

## Conclusion

This project demonstrates how preprocessing, exploratory analysis, and model selection affect predictive performance and interpretability. Progressing from linear regression to polynomial interactions and Gradient Boosting allowed for better accuracy and a clearer understanding of feature importance.  

Through this project, I learned how feature engineering, interaction terms, and advanced models like Gradient Boosting can reveal complex relationships in real-world datasets. I also gained experience in interpreting model results, performing residual analysis, and assessing feature importance.  

For future improvement, I could calculate additional performance metrics beyond R², such as RMSE or MAE, to better evaluate model accuracy. I could explore more in-depth linear regression diagnostics and assumptions, and work on translating insights into practical applications, such as healthcare cost prediction tools or policy analysis frameworks. This would make the analysis more actionable and closer to real-world use cases.
