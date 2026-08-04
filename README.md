<div align="center">

# Predicting U.S. Bank Stock Returns Using Econometric and Machine Learning Models Across Market Regimes

### A Comparative Research Framework for Financial Time-Series Forecasting

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)]()
[![Machine Learning](https://img.shields.io/badge/Machine-Learning-orange)]()
[![Econometrics](https://img.shields.io/badge/Econometrics-ARIMAX%20%7C%20GARCH-success)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)]()
[![Research](https://img.shields.io/badge/Research-Finance-red)]()

*A unified framework for comparing traditional econometric models and modern machine learning algorithms for forecasting U.S. bank stock returns under different market regimes.*

</div>

---

## Overview

This repository presents a unified framework for forecasting next-day returns of major U.S. bank stocks using both traditional econometric models and modern machine learning approaches.

The study compares ARIMAX, ARMA-GARCH, Elastic Net, XGBoost, LightGBM, and CatBoost under an expanding-window walk-forward validation framework. Model performance is evaluated using statistical metrics, economic backtesting, market regime analysis, and SHAP-based explainability.



## Key Highlights

- Comparison of **ARIMAX, ARMA-GARCH, Elastic Net, XGBoost, LightGBM, and CatBoost**
- Expanding-window Walk-forward Validation
- Market Regime Analysis based on VIX
- Statistical comparison using Diebold–Mariano Test
- Economic Backtesting with transaction costs
- SHAP-based Explainable AI
  

## Research Framework

> **Figure 1** should be placed here (Pipeline Overall Research Framework).

<p align="center">
<img src="results/figures/framework.png" width="95%">
</p>

The complete workflow consists of six major stages:

```text
Data Collection
        │
        ▼
Feature Engineering
        │
        ▼
Walk-forward Validation
        │
        ▼
Model Development
        │
        ▼
Statistical & Economic Evaluation
        │
        ▼
Explainability (SHAP)
```

## Repository Structure

```text
bank-stock-return-forecasting/
│
├── data/                  # Raw and processed datasets
├── notebooks/             # Jupyter notebooks
├── paper/                 # Research paper
├── results/
│   ├── figures/           # Figures used in README and paper
│   └── tables/            # Experimental results
├── requirements.txt
├── LICENSE
└── README.md
```

## Forecasting Models

The proposed framework compares three categories of forecasting models.

| Category | Models |
|------------|-------------------------------|
| Econometric | ARIMAX, ARMA-GARCH |
| Linear Machine Learning | Elastic Net |
| Nonlinear Machine Learning | XGBoost, LightGBM, CatBoost |




## Dataset

The experiments are conducted on three major U.S. commercial banks using daily market and macroeconomic data collected from Yahoo Finance and FRED.

| Dataset | Source |
|----------|------------------------------|
| JPM, BAC, WFC | Yahoo Finance |
| S&P 500 Index | Yahoo Finance |
| CBOE Volatility Index (VIX) | Yahoo Finance |
| Financial Select Sector SPDR ETF (XLF) | Yahoo Finance |
| Effective Federal Funds Rate (EFFR) | FRED |
| 2-Year & 10-Year Treasury Yield | FRED |


## Validation Strategy

Expanding-window walk-forward validation was adopted to simulate real-world forecasting, where future observations are unavailable during model training.

| Fold | Train | Test |
|------|--------|------|
| 1 | 2020–2022 | 2023 |
| 2 | 2020–2023 | 2024 |
| 3 | 2020–2024 | 2025 |


## Evaluation Metrics

Unlike conventional forecasting studies that rely solely on prediction errors, this project evaluates models from **four complementary perspectives**.

| Evaluation Aspect | Metrics |
|-------------------|-----------------------------------------------------------|
| Statistical Performance | RMSE, MAE |
| Directional Forecasting | Directional Accuracy, Precision, Recall, F1-score |
| Statistical Significance | Diebold–Mariano Test (Newey–West Correction) |
| Economic Performance | Net Return, Sharpe Ratio, Maximum Drawdown, Turnover |

This multi-dimensional evaluation provides a more comprehensive assessment of forecasting models than conventional error-based evaluation alone.




## Results

The empirical findings demonstrate that:

- Gradient Boosting models consistently outperform traditional econometric models in directional forecasting.
- Walk-forward validation provides a realistic evaluation under non-stationary market conditions.
- Market regime analysis reveals that forecasting difficulty varies substantially across different volatility environments.
- Improvements in Directional Accuracy contribute more to trading profitability than equivalent improvements in RMSE.
- SHAP analysis shows that feature importance changes dynamically across market regimes.


###  Equity Curve

> Replace the figure below with your final equity curve.

<p align="center">
<img src="results/figures/equity_curve.png" width="90%">
</p>



### Explainable AI

Model interpretability is performed using **SHapley Additive exPlanations (SHAP)**.

Two complementary analyses are included:

- Global SHAP
- Regime-specific SHAP

This enables interpretation of how feature importance evolves across different market conditions.

> Replace with your SHAP summary figure.

<p align="center">
<img src="results/figures/shap_summary.png" width="90%">
</p>



## Installation

Clone the repository

```bash
git clone https://github.com/<your_username>/bank-stock-return-forecasting.git

cd bank-stock-return-forecasting
```

Install dependencies

```bash
pip install -r requirements.txt
```

## Quick Start

```bash
# Clone repository
git clone https://github.com/<your_username>/bank-stock-return-forecasting.git

# Enter project directory
cd bank-stock-return-forecasting

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook
```



## Paper

The complete research paper is available in:

```text
paper/
    paper.pdf
```








## License

This project is released under the **MIT License**.

See the [LICENSE](LICENSE) file for details.



</div>
