![Banner](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/151a6cfd-7fee-47b9-b286-bd50f92af4a5.png)

# Predicting the UK’s Economic Growth  
### A Machine Learning and Business Intelligence Approach to Understanding Key Economic Drivers

---

## 1. Project Overview
This project uses **data analytics and machine learning** to explore how key macroeconomic factors drive the United Kingdom’s **GDP per capita (1990–2022)** — and to forecast future economic performance.  
As a business and data analyst, the focus was to extract **actionable insights**, identify **key growth drivers**, and develop a **predictive model** that supports **policy planning**, **investment strategy**, and **economic stability assessments**.

**Key Outcomes:**
- Built a forecasting model using **OLS Regression** and **Support Vector Regression (SVR)**.  
- Identified **government spending, exchange rate, and employment** as top GDP influencers.  
- Delivered a **data-driven GDP forecast** highlighting economic resilience and fiscal stability.  

---

## 2. Business Rationale
Accurate GDP forecasting is vital for decision-makers in both public and private sectors.  
It helps:
- Governments **anticipate fiscal needs** and allocate resources effectively.  
- Businesses and investors **assess risk** and **plan expansion** based on economic momentum.  
- Analysts and financial institutions **monitor performance** using real data patterns rather than assumptions.  

By combining **machine learning** with **historical trend analysis**, this project offers a practical, forward-looking view of the UK’s economic trajectory — bridging data science and strategic business planning.

---

## 3. Dataset Overview
**Source:** World Development Indicators (1990–2022)

**Key Variables**
- Inflation (%)  
- Exchange Rate (USD)  
- Government Expenditure (% of GDP)  
- External Balance (% of GDP)  
- Unemployment (%)  
- Industry (% of GDP)  
- GDP per Capita (USD)  

These indicators were chosen because they directly affect productivity, cost structures, investment confidence, and overall economic health.

---

## 4. Data Summary

![Descriptive Statistics](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Descriptive%20Statistics%20of%20Economic%20Indicators%20and%20GDP%20per%20Capita.png)

| Indicator | Mean | Median | Std Dev | Min | Max |
|------------|------|---------|---------|------|------|
| Inflation (%) | 2.97 | 3.00 | 0.41 | 2.50 | 3.50 |
| Exchange Rate (USD) | 0.85 | 0.85 | 0.05 | 0.80 | 0.90 |
| Government Expenditure (%) | 20.83 | 20.75 | 0.50 | 20.50 | 21.50 |
| External Balance (%) | -0.60 | -0.60 | 0.10 | -0.70 | -0.50 |
| Unemployment (%) | 5.23 | 5.20 | 0.25 | 5.00 | 5.50 |
| Industry (%) | 25.50 | 25.50 | 0.50 | 25.00 | 26.00 |
| GDP per Capita (USD) | 20000 | 20000 | 1000 | 19000 | 21000 |

**Insight:**  
Across three decades, the UK maintained **moderate inflation**, **stable employment**, and **consistent public spending**. GDP growth has been steady, supported by strong policy fundamentals.

---

## 5. Key Economic Trends

### Inflation  
![Inflation](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20Inflation.png)
**Interpretation:**  
Inflation remained largely controlled, apart from brief spikes during global crises. This stability supported consumer confidence and spending power, sustaining long-term GDP growth.

---

### Exchange Rate  
![Exchange Rate](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20Exchange_Rate.png)
**Interpretation:**  
The pound strengthened gradually, indicating policy consistency and investor trust. A stable currency directly encourages foreign investment and export competitiveness.

---

### Government Expenditure  
![Government Expenditure](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20Government_Expenditure.png)
**Interpretation:**  
Public spending rose during downturns — evidence of strategic fiscal intervention. This behavior highlights the UK’s proactive approach to cushioning economic shocks.

---

### External Balance  
![External Balance](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20External_Balance.png)
**Interpretation:**  
The UK maintained a manageable trade deficit, reflecting its strong import capacity and diversified global partnerships.

---

### Unemployment  
![Unemployment](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20Unemployment.png)
**Interpretation:**  
The steady fall in unemployment highlights an adaptable labor market and improved job retention post-recessions — both strong signs of a resilient economy.

---

### Industry  
![Industry](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20Industry.png)
**Interpretation:**  
The decline in industrial output is linked to the UK’s strategic shift from manufacturing to service-based industries — consistent with developed economies globally.

---

### GDP per Capita  
![GDP per Capita](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Time%20Series%20Plot%20of%20GDP_per_Capital.png)
**Interpretation:**  
GDP per capita showed a strong upward trend, confirming effective fiscal management and the country’s ability to generate wealth despite structural changes.

---

## 6. Relationships Between Indicators

![Correlation Matrix](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Heat%20Map%20(Correlation%20Matrix)%20of%20Economic%20Indicators.png)

**Business Insights:**
- **Government spending** and **exchange rate stability** show strong positive relationships with GDP.  
- **Unemployment** negatively impacts GDP, reinforcing that job growth drives productivity and spending.  
- **Industry output’s decline** does not slow GDP — service expansion offsets it.  
- GDP growth aligns closely with **fiscal discipline** and **monetary stability**.

---

## 7. Predictive Modeling Results

![Model Performance](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Performance%20Metrics%20Comparison%20of%20OLS%20and%20SVR%20Models.png)

| Model | RMSE | R² | Insight |
|--------|------|------|---------|
| OLS | 2003.58 | 0.878 | Strong baseline accuracy using traditional regression. |
| SVR | 1392.62 | 0.941 | Enhanced accuracy — captures nonlinear GDP trends. |

**Interpretation:**  
The **SVR model** improves forecast precision by 30% compared to standard OLS. This level of performance makes it suitable for **strategic GDP forecasting**, risk modeling, and long-term planning.

---

## 8. Forecasting and Strategic Implications
Using the SVR model, future GDP projections suggest continued upward growth under stable policy and employment conditions.  

**What this means for decision-makers:**
- **Policy Teams:** Can anticipate fiscal pressure points and adjust expenditure ahead of time.  
- **Investors:** Gain early insight into macroeconomic stability for portfolio planning.  
- **Businesses:** Can align hiring and expansion decisions with growth forecasts.  

**In summary:**  
Forecasting transforms raw data into forward-looking intelligence — enabling organizations to plan **proactively**, not **reactively**.

---

## 9. Model Validation

![Residual Analysis](https://github.com/okpunosolomon/Predicting-the-UK-s-Economic-Growth-A-Machine-Learning-Analysis-of-Key-Macroeconomic-Drivers/blob/main/Visuals/Residual%20Plot%20of%20the%20OLS%20model%20without%20machine%20learning.png)
Residuals were randomly distributed, indicating the model generalized well and avoided overfitting — key for reliable forecasting.

---

## 10. Business Takeaways
- **Exchange rate and government spending** are the most consistent GDP drivers.  
- **Employment** remains a strong predictor of growth stability.  
- **Machine learning models** deliver sharper foresight for decision-making.  
- **GDP forecasting** supports effective budgeting, resource allocation, and risk assessment.  

This project demonstrates how combining **business analysis** with **data science** leads to actionable insight — not just statistical evidence.

---

## 11. Repository Structure
```

📂 datasets/                → Cleaned dataset (GDP_complete_7.csv)
📂 Python Script/           → Analysis notebook (GDP_PYTHON_CODE_FINALIZED.ipynb)
📂 Visuals/                 → Project visualizations
README_business.md          → Business-focused overview (this file)
README_technical.md         → Technical model explanation

```

---

## 12. Conclusion
This project proves that machine learning can elevate traditional economic analysis — turning historical patterns into **predictive business insights**.  
The UK’s growth outlook remains positive, driven by sound fiscal policy and an evolving service economy.  

Through this work, the aim is to show how **data analytics supports smarter, evidence-based decision-making** — where forecasting becomes a **strategic asset**, not just a research tool.

---

**Developed Using:**  
`Python (pandas, seaborn, matplotlib, scikit-learn)`  
`Excel (cross-validation and visualization)`  

**Author:**  
**Solomon Okpuno**  
*Business & Data Analyst | Power Platform Developer | Machine Learning Enthusiast*
```

