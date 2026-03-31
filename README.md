# Market Risk Analysis – CAC40, S&P500 & EUR/USD

## Summary

This project analyzes the market risk of three major financial assets:
- CAC 40 
- S&P 500 
- EUR/USD 

The objective is to measure and compare their:
- Volatility
- Correlation
- Downside Risk (Value at Risk – VaR 95%)

The analysis demonstrates diversification effects and relative risk levels between equity indices and FX markets.

## Dataset

Daily historical data including:
- Date
- Open
- High
- Low
- Close (Price)
- Volume
- Percentage Change

Only closing prices were retained to compute daily returns.

## Methodology

### Data Cleaning
- Date conversion to datetime format
- Removal of commas in price values
- Numeric conversion
- Missing value handling

### Return Calculation

Daily returns computed using:

R_t = (P_t - P_t-1) / P_t-1

### Descriptive Statistics
- Mean return
- Standard deviation (volatility)
- Maximum and minimum returns

### correlation Analysis
- Pairwise correlation
- Correlation matrix

### Historical Value at Risk (95%)

VaR is computed using the 5th percentile of the return distribution:

VaR_95% = Quantile(5%)

## Key Results

| Asset   | Mean Return | Volatility | Min | Max | VaR 95% |
|----------|------------|------------|------|------|----------|
| CAC40    | -0.12% | 0.48% | -1.41% | 0.67% | -0.83% |
| S&P500   | -0.13% | 0.43% | -0.82% | 0.75% | -0.75% |
| EUR/USD  | 0.05%  | 0.18% | -0.43% | 0.31% | -0.29% |


## Risk Interpretation

- Equity indices exhibit higher volatility than FX.
- CAC40 and S&P500 show moderate positive correlation (~0.40).
- EUR/USD provides partial diversification.
- VaR 95% estimates potential daily loss under normal market conditions.

## Technical Stack

- Python
- Pandas
- NumPy
- Matplotlib



