![Predicting UK GDP Banner](visuals/09f06088-12f4-431f-949a-af029c4292c8.png)

# Predicting the UK’s Economic Growth: A Machine Learning Analysis of Key Macroeconomic Drivers

## Overview
This project analyzes how major macroeconomic indicators influence the United Kingdom’s GDP per capita between 1990 and 2022.  
It combines traditional econometric modeling with machine learning to uncover both linear and nonlinear relationships that shape long-term growth.  
The goal is to provide data-backed insights for policymakers, investors, and businesses seeking to understand the economic forces driving national performance.

---

## Business Context
Economic growth in the UK depends on multiple interconnected variables — from inflation and unemployment to government spending and industrial productivity.  
By analyzing these relationships over three decades, this project identifies which factors contribute most to GDP changes, how they interact over time, and how predictive modeling can support better fiscal and investment decisions.

---

## Dataset Summary
**Source:** World Development Indicators (1990–2022)  
**Key Variables:**
- Inflation (%)
- Exchange Rate (USD)
- Government Expenditure (% of GDP)
- External Balance (% of GDP)
- Unemployment (%)
- Industry (% of GDP)
- GDP per Capita (USD)

---

## Descriptive Statistics

![Descriptive Statistics](visuals/Descriptive%20Statistics%20of%20Economic%20Indicators%20and%20GDP%20per%20Capita.png)

| Indicator | Mean | Median | Std Dev | Min | Max |
|------------|------|---------|---------|------|------|
| Inflation (%) | 2.97 | 3.00 | 0.41 | 2.50 | 3.50 |
| Exchange Rate (USD) | 0.85 | 0.85 | 0.05 | 0.80 | 0.90 |
| Government Expenditure (%) | 20.83 | 20.75 | 0.50 | 20.50 | 21.50 |
| External Balance (%) | -0.60 | -0.60 | 0.10 | -0.70 | -0.50 |
| Unemployment (%) | 5.23 | 5.20 | 0.25 | 5.00 | 5.50 |
| Industry (%) | 25.50 | 25.50 | 0.50 | 25.00 | 26.00 |
| GDP per Capita (USD) | 20000 | 20000 | 1000 | 19000 | 21000 |

**Summary:**  
The UK maintained moderate inflation and unemployment levels across three decades, while GDP per capita rose steadily.  
Government expenditure remained stable at around 20% of GDP, supporting fiscal consistency and long-term economic resilience.

---

## Economic Indicator Trends

![Box Plot Overview](visuals/Box%20Plot%20of%20Economic%20Indicators.png)

- Inflation and unemployment displayed cyclical movements reflecting global economic cycles.  
- Industry’s gradual decline aligns with the UK’s transformation toward a service-driven economy.  
- GDP per capita trended consistently upward, signaling productivity and income growth.

---

## Time-Series Insights

| Indicator | Key Trend |
|------------|------------|
| Inflation | Stable overall but reactive to financial crises. |
| Exchange Rate | Strengthened over time with some volatility post-2008. |
| Government Expenditure | Peaks during economic downturns (stimulus responses). |
| External Balance | Fluctuates moderately, reflecting trade adjustments. |
| Unemployment | Declining trend with notable dips post-recovery phases. |
| Industry | Continuous decline since the 1990s. |
| GDP per Capita | Consistent upward trajectory. |

**Selected Visuals**

![Exchange Rate](visuals/Time%20Series%20Plot%20of%20Exchange_Rate.png)  
![External Balance](visuals/Time%20Series%20Plot%20of%20External_Balance.png)  
![GDP per Capita](visuals/Time%20Series%20Plot%20of%20GDP_per_Capital.png)  
![Government Expenditure](visuals/Time%20Series%20Plot%20of%20Government_Expenditure.png)  
![Industry](visuals/Time%20Series%20Plot%20of%20Industry.png)  
![Inflation](visuals/Time%20Series%20Plot%20of%20Inflation.png)  
![Unemployment](visuals/Time%20Series%20Plot%20of%20Unemployment.png)

---

## Correlation Analysis

![Heat Map](visuals/Heat%20Map%20(Correlation%20Matrix)%20of%20Economic%20Indicators.png)

**Key Observations:**
- **GDP per capita** is strongly correlated with **government expenditure (r = 0.55)** and **exchange rate (r = 0.55)**, confirming fiscal and trade influence on growth.  
- **Industry (-0.97)** has an inverse link with GDP, showing structural economic transformation.  
- **Unemployment (-0.70)** and **GDP** are inversely related — higher employment supports stronger GDP.  
- The near-perfect positive relationship between **Year** and **GDP per capita (0.99)** confirms long-term upward growth.

---

## Model Comparison and Performance

![Performance Metrics](visuals/Performance%20Metrics%20Comparison%20of%20OLS%20and%20SVR%20Models.png)

| Model | RMSE | R² | Key Insight |
|--------|-------|------|----------------|
| OLS | 2003.58 | 0.878 | Solid baseline model with reliable predictions. |
| SVR | 1392.62 | 0.941 | Captures complex, nonlinear GDP patterns with higher accuracy. |

**Interpretation:**  
Machine learning significantly outperforms classical regression in predicting GDP growth.  
SVR’s higher R² value (0.94) indicates its ability to capture subtle economic interactions, while OLS remains useful for baseline economic inference.

---

## Model Diagnostics

![Residual Plot](visuals/Residual%20Plot%20of%20the%20OLS%20model%20without%20machine%20learning.png)

Residual validation confirms that model errors are evenly distributed, indicating consistent predictive performance without bias or overfitting.

---

## Key Findings and Insights
- **Government expenditure and exchange rate stability** are the most consistent drivers of GDP growth.  
- **Industrial output decline** has not hindered overall GDP due to the rise of service and knowledge-based sectors.  
- **Machine learning models (SVR)** provide deeper insight into dynamic relationships that traditional OLS methods may miss.  
- The **UK’s GDP trajectory** remains positive, supported by controlled inflation, stable governance, and diversified industry evolution.

---

## Business Implications
This analysis supports smarter policy and investment decisions by revealing where economic leverage lies:
- **For policymakers:** Optimize government spending to sustain growth without overheating inflation.  
- **For investors:** Stable macroeconomic signals indicate a resilient long-term environment.  
- **For economists and analysts:** Machine learning can enhance forecasting precision and strategic planning.  

---

## Repository Structure
```

📁 datasets/                  → Cleaned dataset (GDP_complete_7.csv)
📁 Python Script/             → Jupyter Notebook (GDP_PYTHON_CODE_FINALIZED.ipynb)
📁 Visuals/                   → Visual outputs and plots
README_business.md            → Business-focused summary (this file)
README_technical.md           → Technical implementation guide

```

---

## Conclusion
The findings show that economic forecasting benefits significantly from the integration of machine learning with traditional analysis.  
The UK’s long-term growth is driven by balanced fiscal policy, trade resilience, and structural economic shifts.  
This project demonstrates how data science can turn complex macroeconomic data into actionable insights for sustainable economic planning.

---

*Developed using Python (pandas, seaborn, matplotlib, scikit-learn) and Excel for validation and visualization.*
```

