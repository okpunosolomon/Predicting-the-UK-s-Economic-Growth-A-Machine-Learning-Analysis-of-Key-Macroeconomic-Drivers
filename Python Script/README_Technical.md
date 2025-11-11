# Predicting the UK’s Economic Growth  
### Technical Implementation Report

---

## 1. Objective
This analysis examines how key macroeconomic variables influence the United Kingdom’s GDP per capita (1990–2022).  
The technical objective was to:
- Build a reproducible machine learning pipeline for GDP forecasting.  
- Compare traditional econometric (OLS) and machine learning (SVR) models.  
- Evaluate feature relationships and predictive accuracy.  

---

## 2. Tools and Environment

**Languages and Frameworks**
- Python 3.11  
- Jupyter Notebook  

**Core Libraries**
| Purpose | Libraries |
|----------|------------|
| Data Processing | pandas, numpy |
| Visualization | matplotlib, seaborn |
| Modeling | scikit-learn |
| Statistical Analysis | statsmodels |
| Validation | train_test_split, cross_val_score |

**Data Source**
- World Development Indicators (World Bank, 1990–2022)  

---

## 3. Data Preparation

### 3.1 Loading and Cleaning
```python
import pandas as pd

data = pd.read_csv("datasets/GDP_complete_7.csv")
data.info()
data.describe()
````

Key cleaning steps:

* Checked for missing values using `isnull().sum()`
* Removed duplicate rows
* Standardized variable names (snake_case)
* Converted years to datetime where necessary
* Scaled features for SVR model compatibility using `StandardScaler`

---

### 3.2 Variables Used

| Feature                | Description                               |
| ---------------------- | ----------------------------------------- |
| Inflation              | Annual inflation rate (%)                 |
| Exchange_Rate          | Average yearly exchange rate (USD)        |
| Government_Expenditure | Government spending as % of GDP           |
| External_Balance       | Trade balance as % of GDP                 |
| Unemployment           | Unemployment rate (%)                     |
| Industry               | Industrial sector contribution to GDP (%) |
| GDP_per_Capita         | Dependent variable – GDP per person (USD) |

---

## 4. Exploratory Data Analysis (EDA)

Descriptive statistics and distribution checks were performed using:

```python
data.describe(include='all')
data.corr()
```

Visuals generated:

* Time series plots for each macroeconomic variable
* Correlation heatmap
* Box plots for spread and variation
* Descriptive summary statistics table

Key observations:

* GDP per capita maintained steady growth over time.
* Industry share declined; service sectors expanded.
* Exchange rate and government expenditure show positive correlation with GDP.

---

## 5. Feature Engineering

1. **Feature Selection**

   * Retained numerical features with correlation > 0.4 to GDP.
   * Checked multicollinearity using Variance Inflation Factor (VIF).
2. **Feature Scaling**

   * Applied `StandardScaler` to normalize input features for SVR model.
3. **Train-Test Split**

   ```python
   from sklearn.model_selection import train_test_split

   X = data.drop(columns=['GDP_per_Capita'])
   y = data['GDP_per_Capita']

   X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
   ```

---

## 6. Model Development

### 6.1 Ordinary Least Squares (OLS)

Used as baseline regression model.

```python
import statsmodels.api as sm

X_ols = sm.add_constant(X_train)
ols_model = sm.OLS(y_train, X_ols).fit()
print(ols_model.summary())
```

* RMSE: 2003.58
* R²: 0.878
* Provided explainable relationships between independent variables and GDP.

---

### 6.2 Support Vector Regression (SVR)

Used to capture nonlinear trends.

```python
from sklearn.svm import SVR
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X_train)

svr_model = SVR(kernel='rbf', C=100, gamma=0.1, epsilon=.1)
svr_model.fit(X_scaled, y_train)
```

Evaluation:

```python
from sklearn.metrics import mean_squared_error, r2_score
import numpy as np

y_pred = svr_model.predict(scaler.transform(X_test))
rmse = np.sqrt(mean_squared_error(y_test, y_pred))
r2 = r2_score(y_test, y_pred)
```

* RMSE: 1392.62
* R²: 0.941

The SVR model improved accuracy by ~30% and captured nonlinear relationships better than OLS.

---

## 7. Model Validation

### Residual Analysis (OLS)

```python
residuals = y_train - ols_model.predict(X_ols)
plt.scatter(ols_model.predict(X_ols), residuals)
plt.axhline(y=0, color='red', linestyle='--')
plt.title('OLS Residual Plot')
```

Residuals were evenly distributed — confirming minimal bias and stable performance.

### Cross-validation (SVR)

```python
from sklearn.model_selection import cross_val_score
scores = cross_val_score(svr_model, X_scaled, y_train, cv=5, scoring='r2')
scores.mean()
```

Mean cross-validation R² ≈ 0.93 confirmed model reliability.

---

## 8. Forecasting

Forecasted GDP per capita for future periods (up to 2025) based on existing trends and SVR predictions.

```python
future_predictions = svr_model.predict(scaler.transform(X_future))
```

Forecast insight:

* GDP expected to continue upward trajectory under stable inflation and employment.
* Model useful for short- to medium-term macroeconomic forecasting.

---

## 9. Performance Comparison

| Model | RMSE    | R²    | Notes                                                        |
| ----- | ------- | ----- | ------------------------------------------------------------ |
| OLS   | 2003.58 | 0.878 | Linear model, interpretable but limited for complex patterns |
| SVR   | 1392.62 | 0.941 | Nonlinear model, higher accuracy for forecasting             |

---

## 10. Reproducibility

**Directory Structure**

```
📂 datasets/              → Raw and cleaned GDP data
📂 Python Script/         → Main Jupyter Notebook (GDP_PYTHON_CODE_FINALIZED.ipynb)
📂 Visuals/               → Generated plots and charts
📄 README_business.md     → Business overview
📄 README_technical.md    → This technical report
```

**How to Run**

1. Clone repository

   ```bash
   git clone https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers.git
   ```
2. Navigate to project directory

   ```bash
   cd Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers
   ```
3. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```
4. Open and execute the Jupyter Notebook

   ```bash
   jupyter notebook GDP_PYTHON_CODE_FINALIZED.ipynb
   ```

---

## 11. Key Technical Insights

* OLS remains effective for interpretability but lacks flexibility with nonlinear economic trends.
* SVR achieved higher accuracy and generalization through radial kernel optimization.
* GDP growth can be modeled successfully through data-driven automation rather than static forecasting.
* Proper scaling and feature selection significantly improved predictive reliability.

---

## 12. Future Improvements

* Integrate **XGBoost** and **Random Forest** for ensemble benchmarking.
* Incorporate **real-time macroeconomic APIs** for dynamic forecasting.
* Deploy dashboard via **Power BI or Streamlit** for policy visualization.
* Use **SHAP values** for explainable AI interpretations.

---

**Author:** Solomon Okpuno
**Role:** Business & Data Analyst | Machine Learning Developer
**Tech Stack:** Python, scikit-learn, pandas, seaborn, Excel
**Contact:** [LinkedIn](https://linkedin.com/in/solomon-okpuno-51a907312)

---

*This technical README is optimized for professional GitHub presentation and reproducibility.*

```
