# Board Dashboard — Financial Data Setup

The board dashboard now supports **Google Sheets** for financial metrics.

## Quick Setup

### 1. Create a Google Sheet with this structure:

| metric | forecast | actual |
|--------|----------|--------|
| revenue | 50000 | 48000 |
| cpm | 3.50 | 3.20 |
| gross_margin_pct | 45 | 42 |
| ai_cost_per_episode | 0.85 | 0.92 |
| non_ad_revenue | 5000 | 4500 |
| runway_months | 18 | 16 |
| cash_on_hand | 500000 | 480000 |
| gross_margin_ex_payroll_pct | 65 | 62 |

**Row 1** = headers (metric, forecast, actual)  
**Row 2+** = data rows

### 2. Publish the sheet as CSV:

1. Open your Google Sheet
2. Go to **File → Share → Publish to web**
3. Select the sheet tab (or "Entire Document")
4. Change format from "Web page" to **CSV**
5. Click **Publish**
6. Copy the URL

### 3. Update the dashboard:

In `board-view.html`, find this line near the top of the `<script>` section:

```javascript
const FINANCE_SHEET_URL = 'https://docs.google.com/spreadsheets/d/e/2PACX-1vSl1S2xPX6hSJvnVuG5rO1tFj8yHuBBLh-qGqV8f1E4K_Example/pub?output=csv';
```

Replace it with your published CSV URL.

---

## Metric Reference

| metric key | Dashboard tile | Format |
|------------|----------------|--------|
| `revenue` | Revenue | Dollar ($50K) |
| `cpm` | Blended CPM (podcasts) | Dollar ($3.50) |
| `gross_margin_pct` | Gross Margin % | Percent (45.0%) |
| `ai_cost_per_episode` | AI Cost per Episode | Dollar ($0.85) |
| `non_ad_revenue` | Non-Advertising Revenue | Dollar ($5K) |
| `runway_months` | Cash Runway (months) | Number (18) |
| `cash_on_hand` | Cash on Hand | Dollar ($500K) |
| `gross_margin_ex_payroll_pct` | Gross Margin (Excl. Payroll) | Percent (65.0%) |

---

## Notes

- Dashboard checks the sheet every 5 minutes
- Leave cells empty or put `—` if no data
- Numbers can be plain (50000) or formatted (50,000) — both work
- The metric column must match exactly (lowercase, underscores)
