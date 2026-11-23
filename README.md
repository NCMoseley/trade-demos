# Trade Demos

Interactive, self-contained HTML simulators for trading-strategy evaluation. Each file runs entirely in the browser — no server, no dependencies, no build step.

## Demos

### `damn2b-aleph-live.html`

Paired MNQ intraday signals replayed on a live account.

- **Signals:** DAMN2B (TP 101t / SL 67t, ~2 trades/day) + ALEPH (TP 180t / SL 40t, ~1 trade/day)
- **Sizing:** configurable % risk per entry, micros-granular
- **Frictions:** 4 ticks slippage + $4 round-turn commission per trade
- **Data:** recorded backtest daily outcomes, replayed in sequence (Nov-2024 → Nov-2026)
- **Controls:** starting balance, risk %, per-signal on/off toggles
- **Output:** equity curve, weekly P&L bars, monthly P&L table, red day/week/month counts, min balance, max drawdown

Open directly (`file://`) or serve statically.

## Caveats

These are **models, not promises**:

- All results assume the recorded backtest edge is real and survives live fills — the single largest risk.
- Slippage/commissions are modeled, not measured.
- Position sizing ignores liquidity limits at scale.
- Visible edge decay in the data (2024–26 vs 2020–22).
