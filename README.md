# Premier League 2024/25 — Season Analysis

Analysis of the 2024/25 English Premier League season using Python and pandas, covering final standings, home advantage, and the title race. Cleaned datasets feed a companion Tableau Public dashboard.

## Overview

The raw data is one row per match (380 matches). This project reshapes it into a **team-level dataset** — one row per team per match (760 rows) — which makes every team statistic a single, clean aggregation. From there it builds the full league table, analyses home vs away performance, and tracks how the title race developed over the season.

## Key findings

- **Liverpool won the title comfortably** — 84 points (25W-9D-4L, +45 GD), finishing 10 points clear of Arsenal. Their cumulative points pull clear from mid-season onward.
- **Home advantage is real but not universal** — home teams won 155 matches to away teams' 132 (40.8% vs 34.7%), yet a quarter of the league performed level or better away from home.
- **Home advantage varied widely by team** — Aston Villa gained the most from playing at home (+14 points vs away), while relegated Ipswich were actually *better away* (-8), a poor home record contributing to their drop.
- **Defensive collapse defined the relegation zone** — Southampton (12 pts, -60 GD), Ipswich, and Leicester all conceded 80+ goals.

## Method

1. **Load & inspect** the raw match data (`E0.csv`, from [football-data.co.uk](https://www.football-data.co.uk/englandm.php)).
2. **Reshape to long format** — split each match into two team-perspective rows so `goals_for`/`goals_against` are always relative to one team.
3. **Derive** result (win/draw/loss) and points per match.
4. **Aggregate** into the final standings table, validated against the official final table.
5. **Analyse** home/away splits and cumulative points over time.
6. **Export** clean datasets for visualisation.

## Files

| File | Description |
|---|---|
| `Premier_league_2025.ipynb` | Main analysis notebook |
| `E0.csv` | Raw source data (one row per match) |
| `team_matches_clean.csv` | Reshaped long-format data (760 rows) |
| `standings_clean.csv` | Final league table |

## Tools

Python (pandas, numpy), Jupyter, Tableau Public.

## Dashboard

Interactive dashboard on Tableau Public: **[View the live dashboard →](https://public.tableau.com/app/profile/konstantinos.ioannou/viz/PremierLeague202425-SeasonAnalysis/01_FinalStandings)**

## Data source

[football-data.co.uk](https://www.football-data.co.uk/englandm.php) — free historical football results and statistics.
## Author

**Konstantinos Ioannou**
[GitHub](https://github.com/Iwankon) · [LinkedIn](https://www.linkedin.com/in/konstantinos-ioannou-17430b301/)
