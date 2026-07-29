# Kazakhtelecom Feedback Dashboard

Interactive HTML dashboard for **external** (public reviews) and **internal** (contact-center) Kazakhtelecom feedback data.

## Live demo

**https://nurbek18.github.io/kt-feedback-dashboard/**

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
| External | ~30,189 |
| Internal | ~1,904,198 |

Note: hour-level heatmaps use internal `start_at` timestamps; external reviews are date-only.
