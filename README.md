# Thesis Repository: Financial Ratios, Valuation Multiples & Life Cycle Stages in Tech

This repository contains the complete Python codebase used for the empirical analysis in the thesis on the topic

_"The Impact of Financial Ratios on Valuation Multiples Across Corporate Life Cycle Stages in the Technology Sector"_

## Repository Structure

```
├── data/                    # Raw and processed datasets
├── scripts/                 # Data collection, cleaning, and analysis scripts
├── results/                 # Output files: regression results, tables
├── visualizations/          # Correlation heatmap, histogram charts and evolution plots
├── README.md                # This file
```

## Project Overview

This project investigates how key financial ratios influence valuation multiples (EV/Sales) across different corporate life cycle stages in the U.S. technology sector. The analysis covers firm-year data from 2020–2024 and uses Python for all data processing and regression modeling.

The project includes:

- **Automated data collection** from the SEC EDGAR API, Yahoo Finance, and StockAnalysis.com  
- **Financial ratio calculation** (profitability, liquidity, leverage, efficiency, and others)  
- **Life cycle classification** based on the **Dickinson (2011)** cash flow pattern framework  
- **Panel regression models** with year fixed effects to test hypothesis  
- **Descriptive statistics and visualizations** of financial variable distributions and dynamics

## Tools & Libraries

- `pandas`, `numpy`, `seaborn`, `matplotlib`
- `statsmodels`, `linearmodels`, `yfinance`
- `tqdm`, `BeautifulSoup`, `requests`
- Data sources: **SEC EDGAR API**, **Yahoo Finance**, **StockAnalysis.com**

## Regression Models

The code estimates three panel regression models with year fixed effects:
1. **Baseline model**: Financial ratios only  
2. **Life cycle model**: Financial ratios + life cycle dummies  
3. **Interactions model**: Financial ratios × life cycle stages  

Each model's outputs (coefficients, standard errors, R², adjusted R²) are saved as `.csv` and `.png` files.

## Notes

- All company identifiers, financial metrics, and classifications are anonymized and derived from public U.S. filings.
- For replication or adaptation, update the `email` variable in API scripts and ensure API limits are respected.

## License

This repository is part of an academic thesis and is intended for educational use.
