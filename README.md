# 🇪🇹 Ethiopian Economic Data Analysis (2010–2024)

## Project Overview

This project analyzes Ethiopia’s macroeconomic performance using real-world data from the World Bank and IMF. It combines economic theory with data science techniques to uncover insights, test relationships, and forecast future trends.

The goal is to move beyond basic analysis and answer key economic questions using data-driven methods.

---

## Objectives

- Understand the structure and trends of Ethiopia’s economy
- Analyze relationships between key macroeconomic variables
- Test economic theories such as the Phillips Curve
- Identify drivers of GDP growth
- Forecast future economic indicators
- Translate data into meaningful economic insights

---

## 📦 Data Sources

### World Bank
- https://data.worldbank.org/country/ethiopia

### IMF
- https://data.imf.org/

---

## Variables Used

### Core Indicators
- GDP Growth (annual %) → `NY.GDP.MKTP.KD.ZG`
- Inflation (CPI, %) → `FP.CPI.TOTL.ZG`
- Unemployment (%) → `SL.UEM.TOTL.ZS`
- Population → `SP.POP.TOTL`

### Advanced Indicators
- Gross Capital Formation (% of GDP) → `NE.GDI.TOTL.ZS`
- Exports (% of GDP) → `NE.EXP.GNFS.ZS`
- Imports (% of GDP) → `NE.IMP.GNFS.ZS`
- Agriculture Value Added (% of GDP) → `NV.AGR.TOTL.ZS`
- Industry Value Added (% of GDP) → `NV.IND.TOTL.ZS`
- Services Value Added (% of GDP) → `NV.SRV.TOTL.ZS`
- Exchange Rate (IMF / National Bank)

---

## Project Structure
```text
ethiopia-economic-analysis/
│
├── data/
│   ├── raw/              # Original downloaded datasets
│   ├── cleaned/          # Processed datasets
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_regression.ipynb
│   ├── 04_forecasting.ipynb
│
├── dashboard/
│   └── (Power BI / Tableau / Streamlit files)
│
├── reports/
│   └── final_report.pdf
│
├── README.md
└── requirements.txt

---

## Analysis Breakdown

### 1. Exploratory Data Analysis (EDA)

- Trend analysis (2010–2024)
- Economic shocks (e.g., COVID-19, inflation spikes)
- Correlation analysis

**Visualizations:**
- Line charts (GDP, inflation, unemployment)
- Scatter plots
- Heatmaps

---

### 2. Econometric Modeling

#### Model 1: GDP Growth Model

```

GDP = β0 + β1(Inflation) + β2(Unemployment) + β3(Investment) + ε

```

 Purpose:
- Identify key drivers of economic growth

---

#### Model 2: Phillips Curve

```

Inflation = β0 + β1(Unemployment) + ε

```

 Purpose:
- Test whether inflation and unemployment have an inverse relationship in Ethiopia

---

### 3. Forecasting

Models used:
- ARIMA
- Prophet

Forecast:
- GDP growth
- Inflation rate
- Unemployment trends

---

### 4. Policy Impact Analysis

- Analyze effects of macroeconomic policies
- Example:
  - Impact of money supply on inflation
  - Exchange rate depreciation and inflation

---

##Tools & Technologies

- Python
  - Pandas
  - NumPy
  - Matplotlib / Seaborn
- Statsmodels (econometrics)
- Scikit-learn
- Power BI / Tableau / Streamlit
- Excel (data cleaning & validation)

---

## How to Run the Project

1. Clone the repository:
```

git clone [https://github.com/your-username/ethiopia-economic-analysis.git](https://github.com/mercycermy/ethiopia_economic_analysis.git)

```

2. Install dependencies:
```

pip install -r requirements.txt

```

3. Run notebooks:
```

jupyter notebook

```

---

##  Key Insights (Example)

- Inflation trends show instability in developing economies
- Weak or inconsistent Phillips Curve relationship
- GDP growth increasingly driven by services sector
- Exchange rate plays a major role in inflation dynamics

---

## Key Takeaways

This project demonstrates:

- Application of economic theory using real data
- Strong data analysis and visualization skills
- Ability to interpret macroeconomic trends
- Forecasting and predictive modeling capability
- Policy-relevant economic insights

---

## Author

**Mihret Tsegaye**  
Economics Student | Data Enthusiast | Future Economist  

---

## Future Improvements

- Add real-time data pipeline using APIs
- Build interactive dashboard (Streamlit)
- Include more macro variables (debt, interest rate)
- Expand to comparative country analysis

---

## If you like this project

Give it a star ⭐ and share your feedback!

```
