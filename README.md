# Lindy Communities — Q2 2026 Marketing Dashboard

Interactive, single-file dashboard covering Q2 2026 marketing performance across the Lindy portfolio (31 properties, 6,426 units). Built from the reconciled Yardi ROI Report, the matured Ad Source Performance Report, and the ILS spend files.

**Repo:** https://github.com/abbygross-lindy/q2marketingdashboard
**Live:** https://abbygross-lindy.github.io/q2marketingdashboard/

## What it shows

- **KPI cards** — vacancy, leases, and per-vacant-unit ratios (tours, leases, apps), each labeled with its data basis.
- **Trend chart** — leads / tours / apps / leases over 18 months, by ad source or property.
- **Top 10 comparison** — properties or channels ranked on the selected metric.
- **Funnel detail** — full lead-to-lease funnel by month.
- **Efficiency table** — spend, cost per lease, and lead-to-tour by channel (ILS-spend basis).

Filters across the top: View (Month / Quarter / Year), Metric, Normalize (Raw / Per vacant unit), Compare by (Ad source / Property), plus toggleable chips for all 16 ad sources and 31 properties.

## Data rules baked in

- **7400 Roosevelt is excluded** from all figures (not present in the data at all).
- **Two sources, never blended into one ratio.** Per-vacant-unit ratios are single-sourced on the ROI Report for both years; matured Ad Source figures (2,868 tours / 569 leases) appear in tooltips. See the Basis key legend near the top.
- **Settling months are flagged.** Apr–Jun 2026 leases and approvals are still settling — those cells carry a badge or asterisk and should not be trended.
- **Efficiency table is ILS-spend basis only.** Non-ILS channels show "non-ILS," not $0.

## Structure

Single self-contained HTML file — no server, no dependencies, no build step. Open it in any browser.

- **Top:** the `DATA` object (all verified numbers). This is the only block edited during content updates.
- **Below:** the rendering engine. Never touched during updates.

## Updating

1. Edit the `DATA` block only.
2. Commit to `main`.
3. GitHub Pages auto-deploys (~60 seconds).
4. The SharePoint Embed web part picks up the change automatically.

## Verified anchors

Every render reproduces the reconciled reports exactly: vacancy −17.4% (405.0 → 334.7), 6,426 units, Ad Source 2,868 shows / 569 leases, 7400 excluded.
