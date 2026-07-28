# Kazakhtelecom Feedback Dashboard

Interactive HTML dashboard for **external** (public reviews) and **internal** (contact-center) Kazakhtelecom feedback data.

## Live demo

`https://nurbek18.github.io/kt-feedback-dashboard/`

## Features

- Filter by source, platform, region, sentiment, CRM category, and month range
- KPI cards, sentiment charts, platform/region breakdowns, category table
- External vs internal comparison
- Dark theme; data embedded in `index.html`

## Regenerate locally

From the parent project:

```bash
python pilot/scripts/build_dashboard_agg.py
python pilot/scripts/compress_dashboard_agg.py
python pilot/scripts/generate_feedback_html_dashboard.py
```

## Data scope

| Source | Records |
|--------|---------|
| External | ~30,189 |
| Internal | ~1,904,198 |
