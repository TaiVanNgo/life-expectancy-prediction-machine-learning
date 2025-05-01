# 🧠 Machine Learning Project: Predicting Life Expectancy

**Author:** Ngo Van Tai  

This project explores the relationship between life expectancy and various socio-economic and health indicators using machine learning techniques. It forms part of the individual assessment for COSC2753 - Machine Learning.

## 🎯 Objectives

- Conduct in-depth exploratory data analysis (EDA) on life expectancy data.
- Clean, transform, and prepare the dataset for modeling.
- Apply and compare multiple regression models.
- Identify the best-performing model using statistical evaluation metrics.
- Derive insights that explain the factors influencing life expectancy.

## 📚 Dataset

The dataset contains information about life expectancy across various countries from 2002 to 2017. It includes:

- 2,071 observations across 24 variables
- Demographic indicators (e.g., Country, Status, Population)
- Health indicators (e.g., Adult Mortality, HIV/AIDS, Immunization rates)
- Economic indicators (e.g., GDP, Income Composition of Resources)
- Social factors (e.g., Schooling, Alcohol consumption)

## 🔍 Key Findings

- The target variable shows a strong negative correlation (-0.65) with Adult Mortality and HIV/AIDS (-0.75)
- Strong positive correlation with Income Composition of Resources (+0.74) and Schooling (+0.71)
- Developed countries show significantly higher life expectancy than developing countries
- Life expectancy has shown an upward trend from 2002 to 2017
- Feature importance analysis revealed that Income Composition, HIV/AIDS, and Adult Mortality are the most influential predictors

## 🧹 Data Preprocessing

- **Missing Value Treatment**: Year-wise mean imputation after BMI column removal
- **Outlier Detection**: Applied IQR method (Tukey's) to identify outliers
- **Outlier Treatment**: Used Winsorization to cap extreme values
- **Feature Selection**: Removed highly correlated features to address multicollinearity
- **Feature Scaling**: Standardized features using Z-score normalization

## 🤖 Models Implemented

| Model | R² Score | RMSE | MAE |
|-------|---------|------|-----|
| Random Forest | 0.9014 | 2.9191 | 2.2594 |
| XGBoost | 0.8994 | 2.9476 | 2.2839 |
| Decision Tree | 0.8564 | 3.4813 | 2.6941 |
| KNN | 0.8344 | 3.7419 | 2.9129 |
| Ridge | 0.7933 | 4.1718 | 3.2675 |
| Linear Regression | 0.7929 | 4.1772 | 3.2642 |
| Lasso | 0.7928 | 4.1789 | 3.2652 |
| Polynomial Regression (Degree=2) | 0.7855 | 4.2545 | 3.3280 |
| Polynomial Regression (Degree=3) | 0.7792 | 4.3213 | 3.3793 |
| SVR | 0.7629 | 4.4820 | 3.5225 |

## 🏆 Best Model

**Random Forest** achieved the highest performance with:

- R² Score: 0.9014
- RMSE: 2.9191
- MAE: 2.2594

This model was selected due to:

- Superior performance across all evaluation metrics
- Better suitability for the dataset size (~2,000 rows)
- Acceptable generalization with minimal overfitting
- Good interpretability through feature importance

## 🔧 Tools & Libraries Used

- Python (Jupyter Notebook)
- Data manipulation: Pandas, NumPy
- Visualization: Seaborn, Matplotlib
- Machine Learning: Scikit-learn, XGBoost
- Model persistence: Joblib

## 🚀 How to Run This Project

1. Clone this repository
2. Install required packages: `pip install -r requirements.txt`
3. Open the notebook file `notebook.ipynb`
4. Execute cells in sequence using Jupyter Notebook

## 📊 Key Visualizations

- Correlation matrix of all features
- Feature importance rankings for the best model
- Regression plots comparing actual vs. predicted values
- Distribution plots before and after data cleaning
- Development status impact on life expectancy

## 📬 Contact

If you have questions or would like to connect:

- 📧 Email: [vantaingo.056@gmail.com](mailto:vantaingo.056@gmail.com)  
- 💼 LinkedIn: [Tai Ngo](https://www.linkedin.com/in/taivanngo)  
- 💻 GitHub: [TaiVanNgo](https://github.com/TaiVanNgo)
