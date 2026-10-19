# QuantStack

> **No hype. Just code.**
> The code behind the QuantStack YouTube channel: real costs, unfiltered results, including when the strategy fails.

**Channel:** https://www.youtube.com/@QuantStackDev

## What's here

| Folder | What it is | Needs market data? |
|---|---|---|
| [`audits/breakout-strategy-audit/`](audits/breakout-strategy-audit/) | 7 YouTube breakout strategies + 1 control, one framework, 7 USD majors, realistic costs | Yes (free OANDA practice account) |
| [`tutorials/backtest-report-explained/`](tutorials/backtest-report-explained/) | 6-part series: how to read every number in a backtest report, each metric coded and checked by hand | No |

New to this? Start with `tutorials/backtest-report-explained`: it needs no account or data.

## How the repo is organised

```
audits/       strategy audits (one folder per video or series)
tutorials/    concept and coding tutorials
```

Each project folder is self-contained: its own README, `requirements.txt` and notebook. Run it from inside that folder.

## Setup (any project folder)

```bash
git clone <this repo>
cd <project folder>
python -m venv .venv && source .venv/bin/activate      # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

Launch Jupyter from inside the project folder so relative paths (`data_cache/`, CSV files) resolve.

## Corrections

If I find a bug, I fix it and log it in that project's README, with what changed and why. Open an issue if you find one first.

## Disclaimer

Educational research, not financial advice. Backtests are not predictions. Nothing here is a recommendation to trade. Strategy ideas belong to their original creators; this repository contains my audit framework, not their code.
