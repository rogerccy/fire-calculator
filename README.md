# FIRE Calculator

A Financial Independence, Retire Early calculator. Enter your numbers and instantly see your FIRE target, how many years away you are, and a chart of your portfolio growing to meet it.

**Live:** https://rogerccy.github.io/fire-calculator/

## Features

- **Live calculation** — results and chart update as you type, no submit button needed
- **FIRE number** — calculated as annual expenses ÷ safe withdrawal rate (default 4%)
- **Progress ring** — animated circular indicator showing what percentage of your FIRE number you've already saved
- **Years to FIRE + FIRE age** — exact projection based on your savings rate and expected returns, accounting for compound growth on existing savings
- **Income split bar** — visual breakdown of how much of your income goes to savings vs expenses
- **Portfolio growth chart** — SVG line chart showing your savings compounding year by year, with:
  - Dashed amber line at your FIRE target
  - Amber dot where your portfolio crosses the FIRE line
  - Milestone markers at 25%, 50%, and 75% of the journey
- **Adjustable assumptions** — expected annual return (1–12%, real/inflation-adjusted) and safe withdrawal rate (2–6%) via sliders
- **Edge case handling** — shows a success banner if you've already reached FIRE, and a warning banner if expenses exceed income
- **GitHub Gist sync** — all inputs are saved to a private Gist (`fire-settings.json`) with a 1.2s debounce, syncing across devices
- **Local fallback** — works without a GitHub account via `localStorage`

## Inputs

| Field | Default | Notes |
|---|---|---|
| Current age | 30 | |
| Annual income (after tax) | $80,000 | |
| Annual expenses | $40,000 | |
| Current savings / investments | $20,000 | |
| Expected annual return | 7% | Real (inflation-adjusted) |
| Safe withdrawal rate | 4% | The classic 4% rule |

## Setup

1. Open the app and paste a GitHub Personal Access Token with `gist` scope ([create one here](https://github.com/settings/tokens/new?scopes=gist&description=fire-calculator))
2. Enter your numbers — results appear immediately
3. Settings auto-save to a private Gist after you stop typing

On a new device, enter the same token and the app restores your inputs automatically.
