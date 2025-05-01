# 52-week-breakout-strategy
Momentum-based trading strategy using 52-week highs and volume confirmation to backtest breakout performance on equity data.

---

## Data

All historical return and price data used in this strategy is stored in the `data/` folder:

- `data/djia_data.csv`: Historical price data for DJIA constituents (1998–2024)
- `data/fama_french_49.csv`: Monthly returns from Kenneth French’s industry portfolios

---

## Objective

This project evaluates three trading strategies on the Dow Jones Industrial Average ETF (DIA) and its components over 27 years (Jan 20, 1998 – Dec 31, 2024). It compares passive investing vs. breakout-based active strategies under various market regimes including the dot-com bubble, 2008 crisis, and post-COVID recovery.

---

## Strategies Analyzed

### Strategy 1: Buy & Hold DIA
- $10,000 grows to $95,592  
- **Total Return**: 855.93%  
- Performs best in long-term bull markets but suffers large drawdowns  
- Best suited for investors comfortable with volatility

### Strategy 2: Breakout on DIA ETF
- **Total Return**: -16.84%  
- Avoids major crashes but also misses upside  
- Strategy performance weakens due to poor short positioning and false signals  
- Could be improved by staying in cash or refining entry signals with volume filters

### Strategy 3: Breakout on DJIA Constituents
- $10,000 grows to $46,734  
- **Total Return**: 367.34%  
- Benefits from stock-level rotation  
- Improved risk-adjusted returns compared to Strategy 2

### Strategy 3 (Modified): 11 Newer DJIA Stocks
- Applies breakout to 11 stocks added to DJIA after 1998  
- These stocks contributed significantly to improved performance  
- Not directly comparable to Strategy 2 due to fixed vs. dynamic constituents

---

## Performance Summary

| Metric                      | Strategy 1 | Strategy 2 | Strategy 3 |
|----------------------------|------------|------------|------------|
| Total Return               | 855.93%    | -16.84%    | 367.34%    |
| CAGR                      | 8.74%      | -0.68%     | 5.89%      |
| Sharpe Ratio              | 0.44       | -0.20      | 0.33       |
| Sortino Ratio             | 0.56       | -0.26      | 0.40       |
| Max Drawdown              | -51.87%    | -34.84%    | -49.47%    |
| Beta                      | 1.00       | -0.16      | -0.19      |

---

## Crisis Performance Highlights

- **2000 Dot-Com & 2008 Crisis**:
  - Strategy 1: Deep drawdowns (~50%), 4–5 years to recover
  - Strategy 2: Limited drops (~20%) but flat returns
  - Strategy 3: Sharp drops but recovers faster

- **2020 COVID Crash**:
  - Strategy 1 & 3: Quick rebound
  - Strategy 2: Misses most recovery

---

## Drawdown Analysis

| Strategy | 2000 Drawdown | 2008 Drawdown |
|----------|---------------|---------------|
| Buy & Hold (DIA) | -33.95% | -51.87% |
| Breakout on DIA  | -35.03% | -34.84% |
| Breakout on DJIA | -49.47% | -36.48% |

---

## Conclusion

While breakout strategies can help reduce downside exposure, they often underperform passive strategies in long bull markets. Strategy 3 (breakout on individual stocks) shows promise, especially when refined with better entry signals and stock selection. However, passive investing remains the most consistent wealth-building approach due to its simplicity, compounding, and ability to capture full market upside.

---

## Files

- [`Momentum_Breakout_Strategy.ipynb`](./Momentum_Breakout_Strategy.ipynb): Full code + analysis
- `data/`: Historical equity return datasets
- `.gitignore`, `LICENSE`: Project hygiene and open-source compliance

---

## 👤 Author

Neel Shah  
M.S. Quantitative Finance, Northeastern University  
CFA Level III Candidate | Python, Risk Modeling, Investment Research

