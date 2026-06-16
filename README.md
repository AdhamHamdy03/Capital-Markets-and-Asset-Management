# Capital Markets & Asset Management: Quantitative Labs

> A comprehensive collection of practical Python laboratories focusing on modern portfolio theory, risk management, and quantitative asset pricing models.

## 📖 Overview
This repository contains a series of Jupyter Notebooks demonstrating core concepts in quantitative finance and asset management. The labs bridge the gap between financial theory and practical implementation, utilizing real-world financial data to build, optimize, and evaluate investment portfolios.

---

## 📂 Project Structure

### 1. Portfolio Theory & Optimization
These notebooks explore how diversification changes the risk-return trade-off, advancing from simple two-asset portfolios to complex multi-asset optimization.
* **`Capital_Markets_1.ipynb` & `Risk_revised_v2.ipynb`:** * Maps portfolio weights into mean-volatility space (from 2 assets up to 30 stocks).
  * Constructs the Markowitz Efficient Frontier and Minimum Variance Portfolios.
  * Introduces a risk-free asset to identify the tangency portfolio and plot the Capital Market Line (CML).
* **`Portfolio_Optimization.ipynb`:** * Performs advanced portfolio optimization using the SLSQP algorithm.
  * Implements custom constraints, such as a 10% maximum allocation limit on risk-free assets.
  * Explores weight fluctuations over time using rolling-window optimizations.

### 2. Asset Pricing & Factor Attribution
These notebooks delve into equilibrium pricing models and factor-based performance attribution.
* **CAPM & Security Market Line (SML):** (Covered in `Risk_revised_v2.ipynb` and `Capital_Markets_1.ipynb`) Estimates asset betas and connects them to expected returns via the SML.
* **`multifactor_lab_02c_ff3_clean.ipynb`:** * Explains benchmark-relative performance using the Fama-French 3-Factor (FF3) model.
  * Decomposes active risk (tracking error) for an active portfolio (SPY, VTV, IWM) against a benchmark (SPY).
  * Calculates the share of active variance driven by systematic factors versus residual components.

### 3. Risk Management & Tail Risk Metrics
These labs focus on quantifying and backtesting portfolio risk during normal and stressed market conditions.
* **`Copy_of_one_portfolio_three_vars_one_backtest.ipynb`:** * Computes 1-day 99% Value at Risk (VaR) for a 60/40 (SPY/IEF) portfolio.
  * Compares three VaR methodologies: Historical Simulation, Parametric (Delta-Normal), and Monte Carlo Simulation.
  * Backtests all three methods on a rolling window to track exceptions.
* **`var_vs_expected_shortfall_same_portfolio_revised.ipynb`:** * Compares VaR with Expected Shortfall (ES) on the same 60/40 portfolio to better understand tail severity.
  * Analyzes the gap between ES and VaR and evaluates which metric better captures extreme market events.

---

## 🛠 Technologies & Libraries Used
* **Language:** Python 3
* **Data Manipulation:** `pandas`, `numpy`
* **Optimization & Statistics:** `scipy.optimize`, `scipy.stats`
* **Financial Data Routing:** `yfinance`
* **Data Visualization:** `matplotlib`, `seaborn`

---

## 🚀 How to Run
1. Clone the repository to your local machine.
2. Ensure you have Jupyter Notebook or JupyterLab installed, along with the required libraries:
   ```bash
   pip install pandas numpy scipy matplotlib seaborn yfinance
