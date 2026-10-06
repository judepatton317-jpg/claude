# CEO Dashboard

A single-page tracker for daily sales and acquisition numbers. Open `index.html` in a browser (or use the published artifact link) and enter each day's figures.

## Daily inputs
- # of leads
- # of outbound phone calls
- # of pickups
- # of booked appointments
- # of shown appointments
- # of closed appointments
- Cash collected ($)
- Ad spend for the day ($)

## Monthly inputs
- Software costs ($), which feed CAC
- Cost of goods sold ($), which feeds 30-day gross profit
- "Month is closed": marks CAC as final

## Calculated metrics
| Metric | Formula |
|---|---|
| Qualified lead rate | phone calls ÷ leads |
| Pickup rate | pickups ÷ outbound calls |
| Booking rate (ABR) | booked appointments ÷ leads |
| Show rate | shown appointments ÷ booked appointments |
| Close rate | closed appointments ÷ shown appointments |
| CAC | (month's ad spend + software costs) ÷ closed appointments |
| 30-day gross profit / customer | (cash collected − COGS) ÷ closed appointments |
| Payback ratio | 30-day gross profit per customer ÷ CAC (≥ 1.0x = CAC recovered within 30 days) |
| Days to recover CAC | CAC ÷ (30-day gross profit per customer ÷ 30) |

## Day-by-day history
Every saved day is kept. The history table switches between the selected month and **All days** (grouped by month, with month subtotals and an all-time total). You can:
- **Edit** any day (loads it into the form; saving the same date replaces it)
- **Delete** one day (with an inline confirm), or tick several days and **Delete selected**
- **Export** the month or all days as CSV

Rates show for the month to date and for each day in the log. Each rate is graded against an editable target: green at or above target, amber within 80% of it, red below that.

## Storage
- **Published artifact:** data lives in the artifact's shared database, so it is the same on every device for everyone with access.
- **Opened locally:** data is saved in that browser's local storage only. Use **Export CSV** to back it up.
