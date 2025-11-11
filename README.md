![Predicting UK GDP Banner](visuals/8dd01860-d95f-41a9-86ce-b05113e137be.png)

# Predicting the UK’s Economic Growth: A Machine Learning Analysis of Key Macroeconomic Drivers

## Overview
This project investigates how major macroeconomic variables—such as inflation, unemployment, government expenditure, industry output, and external balance—shape the United Kingdom’s GDP per capita between 1990 and 2022.  
It applies both traditional econometric and modern machine learning models to identify patterns, quantify relationships, and forecast national growth trends.

The aim is to give policymakers, investors, and economic analysts a data-driven understanding of which levers most strongly influence GDP performance and how these drivers interact over time.

---

## Business Context
Understanding what drives a country’s economic growth is crucial for informed decision-making.  
Rising inflation, shifting industry output, or changes in government spending can all affect productivity and household income.  
This analysis uses decades of UK data to measure those effects and to provide insights that can guide economic strategy, fiscal policy, and investment decisions.

---

## Data Summary
Dataset: *World Development Indicators (1990–2022)*  
Variables analyzed include:
- Inflation (%)
- Exchange Rate (USD)
- Government Expenditure (% of GDP)
- External Balance (% of GDP)
- Unemployment (%)
- Industry (% of GDP)
- GDP per Capita (USD)

### Descriptive Statistics
![Descriptive Statistics](visuals/Descriptive%20Statistics%20of%20Economic%20Indicators%20and%20GDP%20per%20Capita.png)

Across three decades, the UK’s average inflation remained stable (≈3%), while GDP per capita grew steadily from around $10,000 to above $35,000. Government expenditure hovered near 20% of GDP, and unemployment showed cyclical trends influenced by broader global conditions.

---

## Key Visual Insights

### 1. Macroeconomic Trends (1990–2022)
![Box Plot Overview](visuals/Box%20Plot%20of%20Economic%20Indicators.png)

- Inflation and unemployment have shown noticeable fluctuations tied to major economic events.  
- Industry’s share of GDP has steadily declined, reflecting the UK’s transition to a service-led economy.  
- GDP per capita shows a consistent upward trend, indicating overall long-term economic growth.

### 2. Time-Series Patterns
Selected time-series plots capture the evolution of key indicators over time:
- **Inflation** shows cyclical volatility, with spikes during financial downturns.  
- **Government expenditure** rises in response to economic shocks, suggesting fiscal countermeasures.  
- **Industry** output trends downward, while **GDP per capita** climbs—highlighting economic restructuring.

---

## Correlation Insights
![Heatmap of Economic Indicators](visuals/Heat%20Map%20(Correlation%20Matrix)%20of%20Economic%20Indicators.png)

- GDP per capita has strong positive links with government expenditure and exchange rate stability.  
- Industry output is negatively correlated with GDP per capita, consistent with the UK’s shift toward services.  
- Inflation and unemployment show modest interaction, reflecting a balanced monetary environment.

---

## Model Comparison: Traditional vs Machine Learning
![Performance Metrics Comparison](visuals/Performance%20Metrics%20Comparison%20of%20OLS%20and%20SVR%20Models.png)

Two models were tested:
- **Ordinary Least Squares (OLS)** regression: baseline for linear relationships.
- **Support Vector Regression (SVR)**: captures complex, nonlinear patterns.

| Model | RMSE | R² | Key Insight |
|-------|------|----|--------------|
| OLS | 2003.58 | 0.878 | Reliable baseline with moderate accuracy |
| SVR | 1392.62 | 0.941 | Higher accuracy; models nonlinear macroeconomic dynamics |

**Interpretation:**  
Machine learning (SVR) significantly improved predictive accuracy, revealing that GDP growth is influenced by nonlinear interactions between macroeconomic drivers—insights that traditional models might overlook.

---

## Residual Validation
![Residual Plot](visuals/Residual%20Plot%20of%20the%20OLS%20model%20without%20machine%20learning.png)

Residual plots confirm the stability of predictions and absence of major bias, validating the robustness of the analysis.

---

## Key Insights & Implications
- **Government expenditure** and **exchange rate stability** are strong predictors of GDP growth.  
- **Declining industrial output** signals the continued rise of services as the UK’s economic engine.  
- **Inflation and unemployment** remain moderate, showing policy consistency across decades.  
- **Machine learning enhances economic forecasting**, enabling better planning for fiscal and investment decisions.

---

## Business Value
This project bridges economic research and practical forecasting, helping:
- **Policy analysts** design better growth and employment strategies.  
- **Investors** understand macroeconomic risks and returns.  
- **Businesses** anticipate long-term trends in productivity and market expansion.  

The results demonstrate how data science supports sustainable economic planning through evidence-based insights.

---

## Repository Structure
```

📁 datasets/                  → Raw and cleaned data (GDP_complete_7.csv)
📁 Python Script/             → Python notebook (GDP_PYTHON_CODE_FINALIZED.ipynb)
📁 Visuals/                   → All figures and model outputs
README_business.md            → Business summary (this file)
README_technical.md           → Technical implementation details

```

---

## Conclusion
The study confirms that data-driven modeling can uncover powerful insights about a nation’s economic performance.  
By integrating classical economics with modern analytics, this project shows how evidence-based intelligence can support strategic planning, investment, and sustainable growth.

---

*Project developed using Python (pandas, matplotlib, seaborn, scikit-learn) and Excel for validation and visualization.*
```

