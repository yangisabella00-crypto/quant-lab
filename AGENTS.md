# AGENTS.md

## Project purpose
This repository is for quantitative research focused on futures markets.

Primary research directions:
- futures contract selection
- trading strategy research
- risk management
- transaction cost modeling
- slippage assumptions
- position sizing
- portfolio exposure control

## Current stage
This repository is currently in the setup and research-design stage.
Do not jump directly into production trading code.
Do not assume live trading, broker APIs, or exchange connectivity.

## Working principles
- Research first, implementation second.
- Keep code transparent, modular, and easy to review.
- Prefer simple Python tools over heavy frameworks.
- Separate clearly:
  - data loading
  - feature/signal generation
  - execution assumptions
  - transaction cost modeling
  - risk management
  - position sizing
  - backtesting
  - reporting

## Market-specific rules for futures
- Explicitly state contract selection logic.
- Explicitly state rollover assumptions.
- Explicitly state whether prices are adjusted or unadjusted.
- Distinguish signal generation from execution timing.
- Avoid look-ahead bias and data leakage.
- Include transaction costs, slippage, turnover, and liquidity considerations where relevant.
- Do not describe a strategy as practical or tradable without robustness checks.

## Risk management standards
When working on any strategy, consider:
- max drawdown control
- volatility control
- stop-loss / exit logic
- leverage assumptions
- margin usage
- concentration limits
- single-instrument risk
- multi-strategy or portfolio exposure

## Coding rules
- Use Python.
- Prefer pandas, numpy, matplotlib, and scipy first.
- Keep functions short and readable.
- Add comments for non-obvious logic.
- Avoid unnecessary dependencies.
- Never fabricate market data.

## Output expectations
When asked to help:
1. explain the task structure first if the task is broad
2. identify assumptions explicitly
3. separate research design from coding
4. summarize risks, limitations, and next steps

## Safety rules
- Never use real broker credentials or private keys.
- Never enable live order execution unless explicitly requested much later.
- Never assume backtest results imply real-world profitability.
