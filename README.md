# PC2 Breastmilk Tracker

A lightweight, mobile-friendly web app to track daily milk output during a 10-day supply boost. No accounts, no subscriptions, no server — just a single HTML file that runs in any browser.

## What it does

- Logs oz pumped and duration (min) for each of 9 daily sessions
- Tracks your schedule: night sessions, power pump, daytime, and evening
- Shows a live summary: total today, sessions done, avg per session, and last session oz
- Charts your output over the last 14 days — by daily total or broken down by session
- Keeps a history table of the last 14 days with notes
- Export and import your data as JSON to move between devices

## Pumping schedule

| Time | Session |
|------|---------|
| 12:00 am | Session 1 — pump before bed |
| 3:00 am | Session 2 — peak prolactin window |
| 6:00 am | Session 3 — morning |
| 8:30 am | Power pump (60 min) |
| 11:00 am | Session 5 — near noon |
| 1:30 pm | Session 6 — post lunch |
| 4:00 pm | Session 7 — afternoon |
| 6:30 pm | Session 8 — post dinner |
| 9:00 pm | Session 9 — last before wind-down |

## How to use

**Live site:** `https://palc2.github.io/breastmilk-tracker`

Or download `index.html` and open it directly in any browser — no install needed.

### Logging a session
1. Open the **Log** tab
2. Navigate to the correct date using the arrows
3. Enter oz and minutes for each completed session — saves automatically as you type
4. Optionally add a day note at the bottom

### Syncing between phone and desktop
Data is stored in your browser's local storage, so phone and desktop don't sync automatically. To move data between devices:

1. On the source device, go to the **Data** tab → tap **Export JSON**
2. Transfer the file (AirDrop, email, etc.) to the other device
3. On the destination device, go to **Data** tab → tap **Import JSON**

Import uses smart merging — if both devices have data for the same session, your existing entries are kept and the conflict count is shown in a summary after import.

## Data storage

All data lives in your browser's `localStorage`. It persists until you clear your browser data. Use the export feature regularly as a backup.

## Tech stack

- Plain HTML, CSS, and JavaScript — no framework, no build step
- [Chart.js](https://www.chartjs.org/) for charts (loaded from CDN)
- Zero dependencies to install

## License

Personal use.
