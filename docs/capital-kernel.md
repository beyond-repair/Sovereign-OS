# Capital Kernel

**Purpose**: Preserve long-term operational viability (INV-008).

## Metrics

- Cash runway (days)
- Burn rate
- Liquidity ratio
- Revenue stability
- Debt exposure
- Risk concentration

## Outputs

- Capital health score
- Allocation recommendations
- Risk alerts

## Invariant

No action may intentionally compromise survivability thresholds.

## Interfaces

- `GET /capital/health`
- `POST /capital/alerts` (configure thresholds)

## Tech

Time-series (InfluxDB / Postgres), forecasting (Prophet/ARIMA), Grafana + Prometheus, PyPortfolioOpt for concentration analysis.
