# Kazakhtelecom Feedback Dashboard

Interactive HTML dashboard for **external** (public reviews) and **internal** (contact-center) Kazakhtelecom feedback data.

## Live demo

**https://nurbek18.github.io/kt-feedback-dashboard/**

## Pages

| URL | Purpose |
|-----|---------|
| [index.html](index.html) | Charts & KPIs (analytics) |
| [records.html](records.html) | **Back-office** row detalization (like Qlik): date, source, sentiment, region, platform, category, topic, text |
| [detail.html](detail.html) | Aggregated pivot tables |

Row data: `data/rows_external.json` (all external) + `data/rows_internal.json` (latest 25k sample of 2.19M internal).

## Features

- **Time dimensions:** year, period (month), date
- **Heatmaps:** weekday × hour, date × hour (internal timestamps)
- **Splits:** by source, platform, city
- **All charts:** Total, Positive, Negative
- **Top 5 categories:** separate rankings for positive and negative
- Global filters: source, platform, city

## Regenerate

```bash
python pilot/scripts/build_dashboard_agg_v2.py
python pilot/scripts/generate_feedback_html_dashboard_v2.py
```

## Data scope

| Source | Records |
|--------|---------|
| External | ~13,766 |
| Internal | ~2,191,434 |

Note: hour-level heatmaps use internal `start_at` timestamps; external reviews are date-only.
