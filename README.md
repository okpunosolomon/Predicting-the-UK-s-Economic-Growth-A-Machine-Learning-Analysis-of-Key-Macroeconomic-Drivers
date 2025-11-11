![Project Banner](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/151a6cfd-7fee-47b9-b286-bd50f92af4a5.png)

# Predicting the UK’s Economic Growth: A Machine Learning Analysis of Key Macroeconomic Drivers

## Overview
This project explores how key macroeconomic indicators influence the United Kingdom’s GDP per capita from 1990 to 2022.  
By combining **econometric methods** with **machine learning models**, the analysis captures both linear and nonlinear relationships that shape the UK’s long-term economic performance.  
The insights are designed for **decision-makers**, **investors**, and **data-driven policy teams** aiming to understand the underlying forces driving GDP growth.

---

## Business Context
The UK’s economy is influenced by complex interactions between inflation, unemployment, trade balance, fiscal spending, and industrial output.  
Through three decades of data, this project investigates how these factors collectively explain shifts in GDP per capita — offering a predictive and interpretive model to support informed decisions in **policy**, **finance**, and **strategic planning**.

---

## Dataset Summary
**Source:** World Development Indicators (1990–2022)  
**Indicators Analyzed:**
- Inflation (%)
- Exchange Rate (USD)
- Government Expenditure (% of GDP)
- External Balance (% of GDP)
- Unemployment (%)
- Industry (% of GDP)
- GDP per Capita (USD)

---

## Descriptive Statistics

![Descriptive Statistics](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Descriptive%20Statistics%20of%20Economic%20Indicators%20and%20GDP%20per%20Capita.png)


**Interpretation:**  
The data reflects a **stable macroeconomic structure**, moderate inflation, and consistent fiscal policy.  
GDP per capita shows steady upward growth, while government spending remains balanced — supporting economic resilience across multiple cycles.

---

## Economic Indicator Trends

![Boxplot Overview](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Box%20Plot%20of%20Economic%20Indicators.png)

**Highlights:**
- Inflation and unemployment exhibit cyclical behavior tied to global recessions and recovery periods.  
- Industry’s steady decline signals the UK’s continued pivot from manufacturing to services.  
- GDP per capita has grown consistently, showing increased national productivity and wealth.

---

## Time-Series Insights

| Indicator | Key Trend |
|------------|------------|
| Inflation | Stable overall, with peaks during crisis years. |
| Exchange Rate | Strengthened post-2008 but shows cyclical fluctuations. |
| Government Expenditure | Increases during downturns, reflecting stimulus policies. |
| External Balance | Moderate fluctuations linked to trade and import-export shifts. |
| Unemployment | Declined steadily over time. |
| Industry | Continuous decline since early 1990s. |
| GDP per Capita | Strong, consistent upward trajectory. |

**Visual Insights:**

![Exchange Rate](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20Exchange_Rate.png)  
![External Balance](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20External_Balance.png)  
![GDP per Capita](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20GDP_per_Capital.png)  
![Government Expenditure](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20Government_Expenditure.png)  
![Industry](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20Industry.png)  
![Inflation](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20Inflation.png)  
![Unemployment](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20Unemployment.png)

---

## Correlation Matrix

![Correlation Heatmap](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Heat%20Map%20(Correlation%20Matrix)%20of%20Economic%20Indicators.png)

**Insights:**
- **GDP per capita** is strongly correlated with **exchange rate (r = 0.55)** and **government expenditure (r = 0.55)**.  
- **Industry (-0.97)** shows a strong negative correlation, highlighting the economic shift toward services.  
- **Unemployment (-0.70)** has an inverse link to GDP — confirming that stronger employment supports national output.  
- The near-perfect correlation between **Year (0.99)** and **GDP per capita** confirms long-term economic growth.

---

## Model Evaluation

![Model Performance](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Performance%20Metrics%20Comparison%20of%20OLS%20and%20SVR%20Models.png)

| Model | RMSE | R² | Key Insight |
|--------|------|------|-------------|
| **OLS** | 2003.58 | 0.878 | Strong baseline model with reliable fit. |
| **SVR** | 1392.62 | 0.941 | Captures nonlinear GDP dynamics, improving accuracy by ~30%. |

**Summary:**  
Machine learning (SVR) clearly outperformed traditional regression.  
Its nonlinear modeling captured subtle macroeconomic shifts that OLS missed — yielding higher predictive accuracy and deeper interpretability.

---

## Diagnostic Validation

![Residual Analysis](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Residual%20Plot%20of%20the%20OLS%20model%20without%20machine%20learning.png)

The residual plot confirms model stability — residuals are evenly spread, indicating minimal bias and no systematic error.

---

## Strategic Insights
- **Fiscal discipline and exchange stability** are the strongest contributors to sustained GDP growth.  
- The UK’s **industrial decline** was offset by expansion in service and technology sectors.  
- **Machine learning models** can enhance forecasting accuracy and guide proactive policy design.  
- Economic resilience is supported by **balanced inflation**, **employment stability**, and **prudent spending**.

---

## Business Implications
This study helps transform economic analytics into practical strategy:

- **For policymakers:** Balance expenditure and inflation control for stable growth.  
- **For investors:** Long-term stability in exchange rate and spending signals investment confidence.  
- **For analysts:** Combining econometric and ML approaches improves macroeconomic forecasting.

---

## Repository Structure
```

📂 datasets/                  → Cleaned dataset (GDP_complete_7.csv)
📂 Python Script/             → Jupyter Notebook (GDP_PYTHON_CODE_FINALIZED.ipynb)
📂 Visuals/                   → Charts and plots
README_business.md            → Business-focused analysis (this file)
README_technical.md           → Technical and modeling documentation

```

---

## Conclusion
Integrating machine learning with economic modeling reveals powerful insights into the UK’s growth trajectory.  
The analysis shows how stable fiscal management, adaptive industrial policy, and consistent exchange rates have driven national prosperity.  
By leveraging predictive analytics, the UK — and similar economies — can strengthen their ability to anticipate economic change and sustain growth.

---

**Developed using:**  
`Python (pandas, seaborn, matplotlib, scikit-learn)`  
`Excel (cross-validation and descriptive review)`
```
