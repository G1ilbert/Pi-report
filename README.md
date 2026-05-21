# Pi-report

Live dashboard for [reportPi](https://github.com/G1ilbert/reportPi) — Raspberry Pi 5 system monitor written in Rust (Axum + SQLite, deployed via Docker scratch image behind Cloudflare Tunnel).

**Live demo:** _(set after Vercel deploy)_
**Backend API:** `https://monitorpi-api.oatori.com`

## Stack
- Single `index.html` (no build step, no framework, no node_modules)
- Vanilla JS + Fetch API for polling
- [Chart.js 4](https://www.chartjs.org/) via CDN for time-series charts
- Pure CSS dark theme, mobile responsive
- Polls backend every 30 seconds

## Deploy on Vercel
1. Import this GitHub repo in Vercel dashboard
2. Framework preset: **Other** (or auto-detected as static)
3. Root directory: `/`
4. Build command: _(none)_
5. Output directory: `/`
6. Deploy

That's it. No environment variables needed (API URL is hardcoded in `index.html`).

## Develop locally
```bash
# any static server, e.g.:
python3 -m http.server 5500
# open http://localhost:5500
```

## Files
| | |
|---|---|
| `index.html` | The whole dashboard — CSS + JS inline |
| `README.md` | This file |
