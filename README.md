# portfolio-diversification-metals
Quantitative analysis of the portfolio diversification benefits of precious metals (Gold, Silver, Platinum).
# Portfolio Diversification with Precious Metals: A Quantitative Analysis

## 📌 Project Overview
This repository contains the advanced quantitative analysis developed for my Master's Thesis. It rigorously evaluates the safe-haven properties and diversification benefits of allocating capital to precious metals (Gold, Silver, Platinum) alongside a traditional 60/40 Equity/Bond portfolio. 

## 📊 Dataset & Assets
Historical market data is automatically fetched via the `yfinance` API, covering the period from January 2000 to March 2026. 

The asset universe includes:
* **Equities:** S&P 500 (`^GSPC`)
* **Bonds:** US Aggregate Bond ETF (`AGG`)
* **Precious Metals (Futures):** Gold (`GC=F`), Silver (`SI=F`), Platinum (`PL=F`)
* **Macro Indicators:** VIX Volatility Index (`^VIX`) and Inflation Proxy (`TIP`)

## ⚙️ Methodology & Advanced Analytics
The codebase executes a comprehensive financial analysis, focusing on risk mitigation and downside protection through several advanced modules:

* **Walk-Forward Out-of-Sample Validation:** Training the models on 2003–2015 data and testing on 2016–2026 to ensure the robustness of the diversification benefit and avoid in-sample overfitting.
* **Macroeconomic & VIX Regime Analysis:** Evaluating how asset correlations shift during different macro environments (Recession, Recovery, Expansion, Inflation Shock) and high/low VIX stress periods.
* **Historical Stress Testing:** Maximum drawdown and waterfall analysis across 5 major historical crises, including the Dot-com crash, 2008 GFC, and the 2022 Inflation Shock.
* **Statistical Robustness:** Implementing non-parametric statistical tests (Mann-Whitney U), Welch's t-test, Jarque-Bera normality tests, and the Jobson-Korkie test to evaluate Sharpe Ratio equality.
* **Portfolio Rebalancing:** Simulating and comparing Buy & Hold strategies versus Annual and Quarterly rebalancing frequencies.

## 🚀 How to Run
The entire analysis is contained within a single Python script. 

1. Install the required dependencies:
   ```bash
   pip install yfinance pandas numpy matplotlib seaborn scipy
   ```
2. Run the script:
   ```bash
   python master_thesis.py
   ```
3. The script automatically generates multiple publication-ready figures and bundles them into a `Master_Thesis_Graphs.zip` archive for easy extraction.
