# Investment Strategy Research — Money Flow Index + Bollinger Bands

A notebook exploring a rule-based market-timing strategy combining the **Money Flow Index (MFI)** and **Bollinger Bands** on SPY price data downloaded with `yfinance`. It calculates indicators, creates trading signals and compares a cumulative strategy-return series with the underlying ETF.

**Technologies:** Python, pandas, NumPy, yfinance, Matplotlib.

## Notebook
- [`MFI_BB.ipynb`](MFI_BB.ipynb) — indicator construction, signal definitions, and return charts.

## Reproduce
Install `requirements.txt` and run the notebook in Jupyter or VS Code with internet access to retrieve market data.

## Research status & limitations
**Exploratory prototype, not an established profitable strategy.** The notebook uses leveraged positions (signals of +3/-3) when both indicators agree. Its current MFI calculation differs from the conventional volume-weighted Money Flow Index: positive/negative sums are computed from typical prices rather than raw money flow, and the final expression differs from the usual `100 - 100/(1 + MFR)`. It has not been verified for realistic trading costs, financing, leverage constraints, data timing, or out-of-sample performance. The chart is illustrative, not independently validated evidence of beating SPY.
