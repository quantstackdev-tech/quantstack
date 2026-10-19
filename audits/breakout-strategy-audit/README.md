# Breakout Strategy Audit

Seven YouTube "breakout strategies", each rebuilt from what its video showed, plus one control strategy built without the flaws, all run through the same engine:

- 7 USD majors, one position at a time ("Global Lock" portfolio)
- next-bar fills, spread, slippage and commission (`EXECUTION_MODE = "production"`)
- fixed-fractional or volatility-scaled sizing (`SIZING_MODE`)
- a ruin floor, bootstrap and Monte Carlo robustness checks, walk-forward folds

**Video:** https://www.youtube.com/watch?v=OBccM0x5CHg&t=8s

## Headline

The control strategy (Strategy 8) over 20 years, real costs: 193 trades, win rate 26.9%, profit factor 0.64, **−34.1%**. Expectancy −0.209 R per trade, 95% bootstrap CI [−0.380, −0.020] — read it as "no demonstrated edge, probably negative". The bootstrap treats trades as independent, so the true interval is wider.

Fill assumption check (receipt R9): filling at the entry bar's midpoint gives −34.1%, at the next open −33.6%, so the headline does not depend on that choice. This check runs on the active strategy only.

Every number the video quotes is printed in the **Findings + receipts** cell (Section 15).

## Run it

```bash
cd audits/breakout-strategy-audit
pip install -r requirements.txt
cp .env.example .env        # fill in your OANDA practice token and account id
jupyter lab Breakout_Strategy_Framework.ipynb
```

**Data is not included.** The notebook downloads price history through OANDA's API and caches it to `data_cache/` on your machine (git-ignored). Results depend on the data window, so yours can differ slightly from the saved run, whose outputs are visible in the notebook.

To run a different strategy, set `ACTIVE_VARIANT` in Section 9d. To compare all eight, use `run_all_strategies()` (Section 9a).

## Exporting the trade log

Section 17 writes `strategy8_trades.csv` and `strategy8_equity.csv`. The `tutorials/backtest-report-explained` notebook reads them in its last section.

## Corrections log

_None yet._

## Notes

The "Video Notes" section at the end is my working notes: claims, each paired with the receipt that backs it.
