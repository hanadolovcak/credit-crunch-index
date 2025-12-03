# Credit Anxiety Index

A financial stress indicator combining credit spreads and Google Trends data to detect early signs of economic slowdown.

## Overview

The Credit Anxiety Index measures market tension by combining credit spread (DBAA - GS10) with Google Trends data for "credit crunch". When both investors and the public grow anxious simultaneously, it often signals trouble ahead.

**Formula:** `Anxiety Index = Credit Spread + (Google Trends / 100)`

## Interpretation

| Index Range | Status | Meaning |
|-------------|--------|---------|
| < 2 | Calm | Stable economy, low risk premium |
| 2-4 | Moderate | Increased caution, rising concern |
| > 4 | High stress | Crisis mode, possible recession signal |

## Historical Context

| Event | Index | Outcome |
|-------|-------|---------|
| 2008 Financial Crisis | ~6.5 | Severe recession |
| 2020 COVID | ~4.3 | Quick recovery with Fed intervention |
| 2025 Current | ~2 | Relatively calm |

## Installation

```bash
pip install -r requirements.txt
```

Required: pandas, matplotlib, plotly, pytrends

## Usage

Run all cells in the notebook. The script downloads FRED data, interpolates GS10 to daily values, fetches Google Trends, and calculates the index.


## Data Sources

**DBAA:** Moody's BAA Corporate Bond Yield (daily) from [FRED](https://fred.stlouisfed.org/series/DBAA)  
**GS10:** 10-Year Treasury Rate (monthly, interpolated to daily) from [FRED](https://fred.stlouisfed.org/series/GS10)  
**Google Trends:** "credit crunch" search volume (3-month rolling window)

## Technical Notes

GS10 data is monthly and linearly interpolated to daily. Google Trends includes retry logic with exponential backoff to handle rate limiting. Historical backfilled data uses 0 for Google Trends since past values cannot be retrieved.

## License

MIT License


## Disclaimer

Educational purposes only. Not financial advice.

## Disclaimer

Educational purposes only. Not financial advice.
