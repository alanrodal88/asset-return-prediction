# Cross-Country Asset Return Prediction with Machine Learning

This project studies whether asset-level characteristics and macroeconomic information can predict next-month excess returns across 50 assets spanning four asset classes and 12 countries.

The analysis compares OLS, Elastic Net, Random Forest, Gradient Boosting, and ensemble models using strictly time-ordered expanding and rolling evaluation schemes. The strongest specification is then translated into a monthly portfolio and evaluated against Equal Weight, Risk Parity, and Time-Series Momentum benchmarks after transaction costs.

## Key Findings

- Asset characteristics contain modest out-of-sample predictive information.
- A 10-year rolling Elastic Net performs better than expanding-window alternatives.
- Global macroeconomic variables improve the preferred Elastic Net specification.
- Country-level macro variables provide little additional forecasting value.
- More flexible nonlinear models and larger predictor sets do not improve out-of-sample performance.
- The forecast-based portfolio achieves lower volatility and drawdown than Equal Weight and a slightly higher Sharpe ratio at low transaction costs.
- Much of the strategy's behavior is closely related to Risk Parity, suggesting that the economic improvement is modest rather than a standalone alpha effect.

## Methods

The project uses:

- OLS
- Elastic Net
- Random Forest
- Gradient Boosting
- Equal-weight forecast ensembles
- Expanding and rolling time-series validation
- Out-of-sample R-squared evaluation
- Transaction-cost-adjusted portfolio backtesting

All predictors are lagged so that only information available before the forecast month is used.

## Files

- [`analysis/ML_Return_Prediction.ipynb`](analysis/ML_Return_Prediction.ipynb) — full analysis and code
- `paper/` — standalone research paper

## Data

The analysis uses an anonymized academic asset and macroeconomic dataset. The raw data are not included in this repository because they were provided for academic use.
