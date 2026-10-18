# Baseball Performance Analytics

Exploratory analysis of MLB batting and salary data using pandas and Matplotlib: home run trends over time, how the Colorado Rockies compare with the league average, and a simple "value for money" metric (on-base percentage per dollar of salary).

## What the notebook does

- Aggregates home runs by season and by team using `groupby`
- Plots total MLB home runs per year to show the long-term trend
- Compares Colorado Rockies home runs per season with the league average per team, from 1993 onward
- Computes on-base percentage (OBP) as `(H + BB + HBP) / (AB + BB + HBP + SF)`, filling missing values and handling players with no plate appearances
- Merges batting data with salary data on player, year and team
- Ranks players by OBP per dollar (minimum 200 at-bats) and looks at the 2010 season

## Findings

- League-wide home runs rose from near zero in the 1870s to roughly 5,500 to 6,800 per season in recent years, with a sharp dip in 2020 (a shortened season).
- The Rockies hit more home runs than the league average per team in several seasons of the late 1990s and mid-2010s, and fewer than average in recent seasons (2021 onward).
- In 2010, the top OBP-per-dollar players were low-salary hitters (around $400k) with OBP between roughly 0.36 and 0.40.

## Data

`Batting.csv` and `Salaries.csv`, with columns such as `playerID`, `yearID` and `teamID`.
Source: *add the link to where you downloaded the data.*

## How to run

1. Open `baseball_analysis.ipynb` in Google Colab or Jupyter.
2. In Colab, upload `Batting.csv` and `Salaries.csv` when the first cell asks. Locally, put both files next to the notebook and remove the `files.upload()` lines.
3. Run all cells.

## Tools

Python, pandas, Matplotlib
