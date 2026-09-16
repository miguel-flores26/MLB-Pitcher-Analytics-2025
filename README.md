# MLB Pitcher Analytics — 2025 Season

An interactive Power BI dashboard analyzing 2025 MLB Statcast pitching data for all 52 "qualified" starting pitchers (minimum 162 innings pitched.

🔗 **[View the live dashboard](https://app.powerbi.com/reportEmbed?reportId=dcb41337-f8a4-41d8-91e8-43225db81065&autoAuth=true&ctid=a8046f64-66c0-4f00-9046-c8daf92ff62b)**

## Overview

This dashboard explores the question: "Which pitchers outperformed or underperformed their underlying skill level in 2025?"

Rather than relying on ERA, which can be heavily influenced by defense, ballpark, and sequencing luck, this analysis uses wOBA vs. xwOBA (a Statcast-based comparison of actual results allowed vs. expected results based on quality of contact) as the primary measure of pitcher skill vs. luck.

## Data

- **Baseball Savant Custom Leaderboard** (baseballsavant.mlb.com), 2025 season, qualified pitchers only
- 52 pitchers, 17 Statcast metrics per pitcher (K%, BB%, ERA, wOBA, xwOBA, exit velocity, barrel rate, hard-hit%, whiff%, chase rate, and more)

## Key Features

- **Leaderboard table** sorted by wOBA − xwOBA, surfacing the season's biggest over/underperformers at a glance
- **Interactive scatter plot** (wOBA vs. xwOBA) with a trend line, showing the full league distribution
- **Click-to-drill-down**: selecting any pitcher updates 8 detail cards covering contact quality (exit velo, barrel%, hard-hit%) and plate discipline (whiff%, chase rate, swing%)

## Key Finding

Nick Pivetta displayed the largest gap between actual and expected performance in 2025 (wOBA - xwOBA of -0.05). This suggests his run prevention was better than the underlying batted-ball data would predict, which could indicate slight positive luck. Meanwhile, there was a four-way tie among Shane Baz, Dylan Cease, Tanner Bibee, and Kyle Hendricks (+0.02) as the season's biggest underperformers by this skill measure. This could suggest the opposite, that they may have had negative luck on defense but could see improved results next season.

## Tools & Skills

- **Power BI** (Power Query / M for data transformation, DAX for measures)
- Data cleaning: converted baseball's non-decimal innings-pitched notation (e.g., "182.1" = 182⅓ innings) into true decimal values for accurate filtering/sorting
- Cross-filtering and interactive drill-down design
