# Backtest Report Explained

A six-part series on reading a backtest report: what each number means, how to code it, and how it can mislead you. One notebook, ending in a single `backtest_report()` function that returns the whole report.

**Playlist link:** [https://www.youtube.com/watch?v=5KLvNsivv1s&t=5s](https://www.youtube.com/playlist?list=PLJbtokAJz9KY)

| Part | Topic |
|---|---|
| 1 | The settings that change every number |
| 2 | Win rate, profit factor and expectancy |
| 3 | Drawdown and the equity curve |
| 4 | Returns and risk-adjusted ratios |
| 5 | Is the result luck? |
| 6 | Is it robust? + the final checklist |

Every metric is first computed on a **toy set of 10 trades you can verify by hand**, with an `assert` that fails if the code disagrees with the hand calculation. Synthetic demo data is seeded and labelled `SYNTHETIC`.

## Run it

```bash
cd tutorials/backtest-report-explained
pip install -r requirements.txt
jupyter lab Backtest_Report_Explained.ipynb     # Restart & Run All
```

No market data or account is needed. The last section runs the report on a real trade log from the breakout audit; if `strategy8_trades.csv` and `strategy8_equity.csv` sit next to the notebook it uses them, otherwise it prints a message and skips that cell.

Parts 3–6 appear on the channel as they are released.

## Corrections log

_None yet._
