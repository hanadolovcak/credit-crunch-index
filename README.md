# credit anxiety index

A financial stress indicator that combines credit spreads and Google Trends data to detect early signs of economic slowdown.


The credit anxiety index measures market tension by combining:
- credit spread (DBAA - GS10) - objective measure of market risk premium
- Google Trends ("credit crunch") - subjective measure of public concern

## Formula
Anxiety index = credit spread + (Google Trends / 100)


## Interpretation

| Index Range | Status | Economic Situation |
|-------------|--------|-------------------|
| **< 2** |  **calm market** | stable economy, low risk premium, relaxed investors |
| **2-4** |  **moderate tension** | increased caution, rising concern, expensive credit |
| **> 4** | **high stress** | serious crisis, panicked investors, possible recession signal |

## Historical context

| Event | Spread | Index | Outcome |
|-------|--------|-------|---------|
| **2008 financial crisis** | ~6% | ~6.5 | Severe recession |
| **2020 COVID** | ~4% | ~4.3 | Quick recovery with Fed intervention |
| **2025 current** | ~2% | ~2 | Relatively calm |
