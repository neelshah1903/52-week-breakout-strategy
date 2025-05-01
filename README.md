# 52-week-breakout-strategy
Momentum-based trading strategy using 52-week highs and volume confirmation to backtest breakout performance on equity data.

## Data

All historical return and price data used in this strategy is stored in the `data/` folder:

- `data/djia_data.csv`: Historical price data for DJIA constituents (1998–2024)
- `data/fama_french_49.csv`: Monthly returns from Kenneth French’s industry portfolios
  
### Objective
This project provides a detailed evaluation of three trading strategies applied to the Dow Jones Industrial Average ETF (DIA) and its underlying components over a 27-year period, from January 20, 1998, to December 31, 2024. The goal is to critically compare passive investing with active, breakout-based strategies to understand their performance across different market conditions.

The analysis examines how simple, rule-based breakout entry and exit signals stack up against a traditional buy-and-hold approach. Rather than focusing solely on absolute returns, it also considers risk-adjusted performance, drawdowns, and long-term portfolio growth. Equal weight is given to assessing how practical, resilient, and adaptable each strategy is during key periods like the dot-com bubble, the 2008 financial crisis, and the post-COVID market recovery.

### Strategies Analyzed
#### Strategy 1: [Figure 1]
Buy & Hold on DJIA ETF graph shows how a portfolio of USD 10,000 invested in DIA from 1998 to 2024 grows to USD 95,592, with a total return of 855.93 %. The chart highlights the absolute growth, revealing a strong long-term upward trend despite some steep dips during major market downturns like 2008 and 2020. Overall, this strategy delivers the highest growth among the three, making it best suited for investors who are focused on long-term returns and comfortable riding out market volatility. 

#### Strategy 2: [Figure 2]
Breakout Strategy on DIA ETF graph shows how the strategy performed from 1998 to 2024 when applied directly to the DIA ETF. Starting with USD 10,000, the portfolio ends lower, with a total return of -16.84% over the full period. The graph shows the cumulative return, and it’s mostly falls less compared to other stratergies with several sharp drops—especially during major market events like 2008. While the strategy does manage to avoid some of the worst market crashes by staying out at times, it also misses the upside, which really hurts its long-term performance.

##### Analysis for Strategy 2 – Source of Returns [Figure 3]
The short positions consistently underperformed, contributing to drawdowns. If, instead of shorting, we had stayed in cash, we could have avoided these losses and improved overall returns. This suggests that the market structure may not favor short trades, or the timing of short entries needs refinement. While long trade contributed positively, they also experienced stagnation at times. This indicates that some breakouts failed to generate strong momentum, possibly due to premature entries or false breakouts. Refining entry criteria—such as incorporating volume confirmation—could help in filtering better trades. Whenever the strategy stayed in cash, it acted as a stabilizing force, preventing unnecessary risk exposure. If a portion of this cash had been allocated to a risk-free asset, the strategy could have earned additional returns without extra risk.

#### Strategy 3: [Figure 4]
Breakout Strategy on DJIA Constituents graph shows how a portfolio of USD 10,000 using this breakout approach on individual DJIA stocks grows to $46,734 between 1998 and 2024, with a total return of 367.34%. The graph highlights growth, showing a generally steady upward trend with some noticeable dips during major market downturns. 

#### Strategy 3 (Modified) : [Figure 5]
This is the breakout strategy applied specifically to the 11 DJIA constituents that were not part of the index in 1998 but there in 2024. This strategy tracks the performance of a fixed set of stocks, excluding those that were part of the DJIA in 1998, thereby highlighting the impact of these stocks on the overall performance. The performance of Stratergy 3 Modified has been high, with these newer stocks contributing positively to returns, which led to a rise in cumulative performance over time.

##### Analysis for Strategy 3
The assumption is that these 11 stocks for modified strategy have been added to the DJIA on average during the analyzed period. Their strong growth in the index have boosted the performance of Strategy 3 compared to other strategies. However, when comparing Strategy 3 with Strategy 2, it’s essential to recognize that Strategy 2’s constituents changed annually, reflecting the dynamic nature of the DJIA. In contrast, Strategy 3 maintained a fixed set of stocks, which makes direct comparison misleading.The positive returns in Strategy 3 may be partially attributed to the influence of these stocks, which were not part of Strategy 2’s changing set of DJIA constituents. Therefore, Strategy 3’s performance cannot be directly compared to Strategy 2.

### Comparison and Results Interpretation
#### A. Performance Metrics [Table 1]
The passive Buy and Hold DIA strategy delivered a Total Return of 855.93% and a CAGR of 8.74%. Its Sharpe (0.44) and Sortino (0.56) ratios reflect risk-adjusted returns and relatively controlled downside risk. Strategy 1 has the market beta of 1. Strategy 2 has a negative beta (-0.16), meaning its returns move slightly opposite to the market. This reflects its defensive design—it avoids major drops by exiting during periods of high risk, helping to reduce drawdowns and preserve capital. Strategy 3 also shows a negative beta (-0.19), suggesting a low and slightly inverse correlation with the broader market. However, its exposure to individual DJIA stocks introduces higher volatility, which explains its deeper drawdowns during extreme events.

The Breakout Strategy on DIA ETF performed poorly, with a Total Return of -16.86% and CAGR of -0.68%. The negative Sharpe and Sortino ratios suggest the strategy suffered from poor timing and too many false signals. Strategy 3, which applied breakout signals to individual DIA stocks, did much better than Strategy 2. It earned a Total Return of 367.25% and a CAGR of 5.89%, showing that trading individual stocks can be more effective than the ETF. Still, its Sharpe and Sortino  ratios were lower than the passive strategy, meaning higher volatility and less efficient returns.

#### B. Comparison of Strategies in Crises Periods [Figure 6]
Shaded areas show major financial crises: the 2000 Dot-Com Bubble, 2008 Financial Crisis, and 2020 COVID Crash. Crises and Recovery: 2000 & 2008: Strategies 1 and 3 fall ~50% but recover in 4–5 years. Strategy 2: Drops only ~20% and stays flat — it avoids big losses but also misses rebounds. 2020 Crash: All strategies take a hit, but 1 and 3 bounce back fast. Strategy 2 stays mostly flat.

#### C. Drawdown Comparison: Buy & Hold vs Breakout Strategies [Figure 7 and Table 2]
Strategy 1 (Buy & Hold DIA) aligns with the Efficient Market Hypothesis (EMH), providing full market exposure but suffering from deep and prolonged drawdowns, such as -33.95% in 2000 (771-day recovery) and -51.87% in 2008. In contrast, Strategy 2 (Breakout on DIA) and Strategy 3 (Breakout on DJIA Constituents) attempt to exploit market inefficiencies. Strategy 2 shows smaller drawdowns (-35.03% in 2000, -34.84% in 2008) than Strategy 3, while Strategy 3, despite managing risk dynamically across stocks, still experiences large swings (-49.47% in 2000, -36.48% in 2008). Overall, the breakout strategies aim to reduce exposure during downturns and capitalize on recoveries, making them more adaptive.

### Conclusion
Passive investing, such as a buy-and-hold approach in the DJIA ETF, often outperforms active strategies due to reduced biases and the ability to capture long-term market growth. The breakout strategy, despite its intent to capitalize on short-term price movements, faces risks like false breakouts, higher volatility, and missed opportunities during sustained bull markets. 

Additionally, active strategies require continuous monitoring and adjustments, which may not always justify the additional effort when broad market exposure historically delivers consistent returns. Over time, the compounding effect of staying invested in the market outweighs the potential gains from frequent trading, making passive investing a more reliable wealth-building approach.
