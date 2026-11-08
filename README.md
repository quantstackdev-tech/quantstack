# QuantStack

> **No hype. Just code.**
> The code behind the QuantStack YouTube channel: real costs, unfiltered results, including when the strategy fails.

**Channel:** https://www.youtube.com/@QuantStackDev

**New to algorithmic trading?** Start with *Start Here: Algorithmic Trading From Zero* (coming soon), then follow the [tutorials table](#tutorials) from the first row to the last.

**Want to see strategies tested?** Go to the [strategy audits](#strategy-audits).

## Table of contents

Coming soon means planned, not promised. A "code" link appears only when the folder exists. The tutorials table lists the Core track only.

### Strategy audits

Each audit is one video, tested in Python with real costs. A new row is added here when an audit is published.

| Playlist | Video | Status |
|---|---|---|
| **Trading Strategy Audits (Python Backtests)** | T3-01 · Seven breakout strategies compared ([code](audits/breakout-strategy-audit/Breakout_Strategy_Framework.ipynb)) | [Watch the video](https://www.youtube.com/watch?v=OBccM0x5CHg) |

### Tutorials

Each playlist, the series inside it, and where each series stands, in viewing order. Published series link to their YouTube playlist; the rest say "In production" or "Coming soon" (0 of 45 series fully published, 5 of 562 videos).

| Playlist | Series | Status |
|---|---|---|
| **Foundations**<br>Start Here: Algorithmic Trading Foundations | **S001** Start Here | In production |
|  | **S011** Jupyter Explained ([code](tutorials/Jupyter Explained/Jupyter_Explained.ipynb)) | In production |
|  | **S012** Python Basics From Zero | In production |
|  | **S020** Markets 101 | In production |
|  | **S021** Brokers, Orders and Costs | Coming soon |
|  | **S022** Reading Charts From Zero | Coming soon |
|  | **S023** Why Most Traders Lose | Coming soon |
|  | **S024** MetaTrader 5 Basics | Coming soon |
|  | **S025** Trade Accounting by Hand | Coming soon |
| **Python and Data**<br>Python and Data for Traders | **S013** Python Intermediate | Coming soon |
|  | **S014** NumPy for Finance | Coming soon |
|  | **S015** pandas for Traders | Coming soon |
|  | **S016** Charts for Traders (matplotlib and plotly) | Coming soon |
|  | **S040** Market Data Done Right | Coming soon |
|  | **S045** FX Data and Costs in Code | Coming soon |
|  | **S017** Git and GitHub for Traders | Coming soon |
| **Maths and Statistics**<br>Maths and Statistics for Quant Traders | **S030** Maths You Need: Algebra to Calculus | Coming soon |
|  | **S031** Probability From Zero | Coming soon |
|  | **S032** Statistics for Traders | Coming soon |
|  | **S036** Financial Maths | Coming soon |
|  | **S035** Time Series Fundamentals | Coming soon |
| **Backtesting**<br>Backtesting Done Right: Build, Test and Trust | **S056** Indicators and Signals From Scratch | Coming soon |
|  | **S050** Build a Backtester From Scratch | Coming soon |
|  | **S055** Testing Your Backtester | Coming soon |
|  | **S052** Backtest Pitfalls | Coming soon |
|  | **S054** Metrics Deep Dive | Coming soon |
|  | **S051** Backtest Report Explained ([code](tutorials/How-to-Read-a-Backtest-Report/Backtest_Report_Explained.ipynb)) | 6 of 6 videos published |
| **Validation, Risk and Portfolios**<br>Is It Real? Validation, Risk and Portfolios | **S070** Is It Real? Validation and Overfitting | Coming soon |
|  | **S071** Edge, Expectancy and Sample Size | Coming soon |
|  | **S072** Robustness Testing Toolkit | Coming soon |
|  | **S073** Honest Verdicts: Putting a Number on Luck | Coming soon |
|  | **S080** Risk Management Fundamentals | Coming soon |
|  | **S081** Position Sizing | Coming soon |
|  | **S082** Drawdown and Ruin Simulation | Coming soon |
|  | **S090** Portfolios of Strategies | Coming soon |
| **Live Trading and Engineering**<br>Live Trading and Trading System Engineering | **S100** Going Live with MT5 and Python | Coming soon |
|  | **S101** Execution Quality and Slippage | Coming soon |
|  | **S102** Trading System Operations | Coming soon |
| **Machine Learning**<br>Machine Learning for Trading, Honestly Tested | **S110** Machine Learning From Zero | Coming soon |
|  | **S111** ML for Trading: Foundations | Coming soon |
|  | **S115** Model Validation for Finance | Coming soon |
|  | **S112** Meta-Labeling and ML Filters | Coming soon |
| **Capstones**<br>Capstones: Build a Complete System | **S180** Capstone 1: A Simple, Honest System | Coming soon |
|  | **S181** Capstone 2: A Validated Rule-Based System | Coming soon |
| **Failure Files and Shorts**<br>Failure Files | **S190** Failure Files | Coming soon |

## How the repo is organised

```
audits/        strategy audits, one folder per tier, one folder per audit inside it
tutorials/     concept and coding series, grouped by YouTube home-tab section
checkpoints/   projects you build alone at the end of a stage   (created when the first one ships)
capstones/     complete systems, judged honestly                (created when the first one ships)
failure-files/ short experiments that test popular claims       (created when the first one ships)
docs/          conventions for naming and project folders
```

Folder names start with the roadmap ID (`s051-`, `t3-01-`), so a series ID in the table leads straight to its code. The numbers inside `tutorials/` match the channel's home-tab sections. Naming rules are in [docs/CONVENTIONS.md](docs/CONVENTIONS.md).

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
