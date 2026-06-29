# Polylog

Static dashboard for polybot paper-trading and research status.

The page reads `summary.json` and refreshes in the browser. Strategy runners do not run in this repo.

## GitHub Actions Publishing

`Publish Dashboard Data` runs every five minutes and pulls `/summary.json` from the VPS read-only endpoint, then commits it to this repo for GitHub Pages.

Required repository variable:

- `SUMMARY_URL`: read-only summary endpoint.

This workflow only publishes dashboard data. It does not use SSH credentials, run Polymarket scanners, research, or live trading.
