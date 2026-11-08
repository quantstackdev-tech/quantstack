# QuantStack

> **No hype. Just code.**
> The code behind the QuantStack YouTube channel: real costs, unfiltered results, including when the strategy fails.

**Channel:** https://www.youtube.com/@QuantStackDev

## Start here (learning order)

The channel teaches in a fixed order. Each row is a folder in this repo, and each folder is self-contained (own README, `requirements.txt`, notebook).

| # | Series | Folder | You need | Status |
|---|---|---|---|---|
| 1 | What Algorithmic Trading Is, and Isn't (1 video) | no code | nothing | in production |
| 2 | Jupyter Explained (6 parts) | [`tutorials/S011-jupyter-explained/`](tutorials/S011-jupyter-explained/) | nothing | in production |
| 3 | Python Basics From Zero (18 parts) | [`tutorials/S012-python-basics-from-zero/`](tutorials/S012-python-basics-from-zero/) | nothing | in production |
| 4 | Markets 101 (14 parts) | no code (concept series) | nothing | in production |
| 5 | Backtest Report Explained (6 parts) | [`tutorials/S051-backtest-report-explained/`](tutorials/S051-backtest-report-explained/) | nothing | Part 1 published |

Strategy audits (apply what the tutorials teach to real strategies):

| Audit | Folder | Needs market data? |
|---|---|---|
| Breakout strategies (7 + 1 control) | [`audits/breakout-strategy-audit/`](audits/breakout-strategy-audit/) | Yes (free OANDA practice account) |
| Trend and moving-average strategies | coming soon (`audits/trend-ma-audit/`) | Yes (same account) |

The full plan, with every series and video, is in [`ROADMAP.md`](ROADMAP.md).

## Which folder first?

Brand new to code: `tutorials/S011-jupyter-explained`, then `S012-python-basics-from-zero`. Already code: `tutorials/S051-backtest-report-explained` needs no account or data, then the audits.

All setup assumes **Windows** (the channel is recorded on Windows). Linux and macOS usually work, but only Windows is tested.

## How the repo is organised

```
tutorials/   one folder per teaching series, named by series ID (S011, S012, S051 ...)
audits/      one folder per strategy audit
ROADMAP.md   every planned series and its status
```

Folder names start with the series ID used on the channel, so video S051-04 is Part 4 of `S051-backtest-report-explained`.

## Setup (any project folder)

```bash
git clone <this repo>
cd <project folder>
python -m venv .venv
.venv\Scripts\activate          # Windows. On Linux/macOS: source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Launch Jupyter from inside the project folder so relative paths (`data_cache/`, CSV files) resolve.

## Corrections

If I find a bug, I fix it and log it in that project's README, with what changed and why. Open an issue if you find one first.

## Disclaimer

Educational research, not financial advice. Backtests are not predictions. Nothing here is a recommendation to trade. Strategy ideas belong to their original creators; this repository contains my audit framework, not their code.
