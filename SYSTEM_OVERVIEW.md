# System Overview (Public Mirror)

## Runtime Ports
- Gateway API: `${GATEWAY_PORT:-7000}`
- Adapter API: `${ADAPTER_PORT:-7001}`
- PM Simulator: `${PMSIM_PORT:-7002}`

> Ports are env-driven via `.env` in the main repo. Public artifacts remain the same.

## Pipeline
1) Data → Indicators/Strategies → Backtest (`backtest_results.csv`)
2) Selection → PM Payload (`pm_candidates.json`)
3) Smoke: POST `/pm/sim` with top candidate

## Artifacts (per release)
- `pm_candidates.json`, `backtest_results.csv`, `indicators_*.csv`
