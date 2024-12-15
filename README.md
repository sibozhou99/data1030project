# README: Predicting Age at Death for Americans Using CDC Mortality Dataset  

## Author  
Sibo Zhou  
Data Science Institute, Brown University  
December 15, 2024  

## GitHub Repository  
Project Repository: 
https://github.com/sibozhou99/data1030project  

## Data Access
Due to GitHub upload limits, the raw and preprocessed datasets are available here: 
https://drive.google.com/drive/folders/1f_GnQ2zj_ifSP8gXqXCMoZ_xFphovCRI?usp=sharing  

## Dataset  
Source: CDC Mortality Dataset (2005–2015)  
Size: 2.7 million rows with detailed records on demographic and health information, including age, sex, race, marital status, education, and causes of death.  

## Python and Package Versions  
The project was developed in Python 3.8.20 with the following packages:  

- pandas: 2.1.0  
- numpy: 1.25.0  
- scikit-learn: 1.3.2  
- xgboost: 2.1.3  
- shap: 0.44.1  
- seaborn: 0.12.2  
- matplotlib: 3.8.0  
- joblib: 1.4.2  
- scipy: 1.10.1  

## Project Overview  
This project explores the relationship between demographic factors and age at death (`age_at_death`) using the CDC's Mortality Dataset (2005–2015). Machine learning models are used to predict age at death based on demographic features, and both global and local feature importance analyses provide insights into mortality trends.  

## Motivation  
Life expectancy in the United States varies significantly across demographic groups. Understanding these disparities can guide public health research and policy efforts to address inequalities related to gender, race, marital status, and ethnicity.  

## Key Results
Model Performance
RandomForestRegressor achieved the lowest RMSE (13.24), outperforming XGBRegressor (13.25) and linear models like Lasso, Ridge, and Elastic Net (13.67).
All models surpassed the baseline RMSE of 17.07.

Feature Importance
Globally, marital status, education level, and sex were the most predictive features across all models.
Locally, SHAP analysis highlighted nuanced impacts, such as the positive influence of being widowed and the negative influence of being single.

## Future Directions
Include non-demographic features, such as health conditions, to improve model accuracy.
Use advanced feature engineering (e.g., interaction terms) and explore deep learning models for better performance.
Incorporate instrumental variables for causal inference to address potential reverse causality.
