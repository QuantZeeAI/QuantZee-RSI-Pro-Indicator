# RSI Pro+ | Divergence + Adaptive Bands + MTF

An RSI (Relative Strength Index) toolkit for TradingView, built by [QuantZee](https://quantzee.com/). It combines three things that are normally three separate scripts:

- **Auto Divergence Engine** — detects regular and hidden bullish/bearish divergences between price and RSI, with non-repainting pivot confirmation
- **Adaptive OB/OS Bands** — overbought/oversold levels computed as rolling percentiles of RSI itself, so they adjust to the current market regime instead of staying fixed at 70/30
- **Multi-Timeframe RSI Dashboard** — an on-chart table showing RSI value + status across 5 configurable timeframes at once

Written from scratch, open source, `@version=6`.

Learn more at [quantzee.com](https://quantzee.com/).

## Features

| Group | What it does |
|---|---|
| RSI Core | Standard RSI with configurable length and source |
| Adaptive OB/OS Bands | Toggle between static 70/30-style levels and percentile-based adaptive bands (lookback + percentile thresholds configurable) |
| Divergence Engine | Regular + hidden divergence detection, pivot lookback/range all configurable, signals confirmed (non-repainting) |
| Multi-Timeframe Dashboard | 5 configurable timeframes, table position configurable, shows RSI value + OB/OS status per timeframe |
| Alerts | 6 built-in alert conditions — regular bullish/bearish divergence, hidden bullish/bearish divergence, RSI exiting overbought, RSI exiting oversold |

## How to use

1. Open **TradingView** → Pine Editor.
2. Copy the contents of [`RSI_Pro_Plus.pine`](./RSI_Pro_Plus.pine) into a new script.
3. Click **Add to Chart**.
4. Configure the input groups (RSI Core, Adaptive OB/OS Bands, Divergence Engine, Multi-Timeframe Dashboard) from the indicator's settings.
5. Right-click the indicator → **Add Alert** to wire up any of the 6 alert conditions to your notification channel of choice.

## Reading the signals

- **Regular bullish divergence** (`Bull` label): price makes a lower low while RSI makes a higher low — often a reversal-up signal.
- **Regular bearish divergence** (`Bear` label): price makes a higher high while RSI makes a lower high — often a reversal-down signal.
- **Hidden divergences** (`H Bull` / `H Bear`, off by default): the inverse pattern — more useful as trend-continuation signals than reversal signals.
- **Adaptive bands**: when RSI crosses back inside the adaptive band from outside it, that's the "RSI Exits Overbought/Oversold" alert — often read as momentum normalizing after an extreme.

## Disclaimer

This indicator is analytical software for charting and research. It is **not investment advice** and QuantZee is not a registered investment advisor. Past performance of any signal or pattern does not guarantee future results. Always do your own research before trading.

## About QuantZee

[QuantZee](https://quantzee.com/) builds a premium suite of TradingView indicators and analytical toolkits — adaptive RSI, trend, and oscillator tools designed to help traders read price action and market structure more clearly. Learn more at **https://quantzee.com/**.

## License

MIT — see [LICENSE](./LICENSE).
