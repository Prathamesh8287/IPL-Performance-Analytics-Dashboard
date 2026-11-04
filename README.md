# 🏏 IPL Performance Analytics Dashboard (Power BI)

An interactive, one-page Power BI dashboard that analyses **1,243 IPL matches (2008–2026)**: scoring trends, toss impact, venues, team performance and top players. It is built on ball-by-ball JSON data from Cricsheet, cleaned in Power Query and modelled with DAX.

![IPL Performance Analytics Dashboard](images/dashboard.png)

> 🎥 Walkthrough video: [add LinkedIn post or video link here]

---

## 📌 Project Overview

| | |
|---|---|
| **Goal** | Turn raw ball-by-ball IPL data into a clear, interactive story about scoring, toss decisions, venues, teams and players |
| **Tool** | Power BI Desktop (Power Query + DAX) |
| **Data** | [Cricsheet](https://cricsheet.org/) IPL ball-by-ball data (JSON) |
| **Coverage** | 1,243 matches, seasons 2008–2026 |
| **Format** | Single-page dashboard, 16:9 (1280 × 720), custom theme |

---

## 🛠️ Tech Stack

- **Microsoft Power BI**: dashboard design and visualization
- **Power Query**: data transformation and cleaning
- **DAX**: measures and calculations
- **Cricsheet**: ball-by-ball IPL match data (JSON)

---

## 📊 What's on the Dashboard

**KPI cards**
- Total Runs: 402K
- Total Matches: 1,243
- Total Fours: 34K
- Total Sixes: 16K
- Avg Runs / Innings: 161.79
- Top Run Scorer and Top Wicket Taker cards that update with the slicers

**Visuals**
- **Total Runs by Season**: columns for total runs, with a line for average score per innings
- **Toss Winner's Match Win % by Decision**: does batting or fielding first after winning the toss lead to more wins? (with a 50% reference line)
- **Top Venues by Matches**: the most-used IPL grounds
- **Team Performance table**: wins, matches, total runs and win %, with data bars on win %
- **Top Batters by runs**, **Top Bowlers by wickets**, **Top Six-hitters**

**Interactivity**
- Season and Team slicers that filter every visual and card

---

## 🔍 Key Insights

1. **Fielding first after winning the toss pays off.** Toss winners who chose to field won **53.7%** of their matches, compared with **44.3%** for those who chose to bat.
2. **Scoring is rising, but total runs can mislead.** Total runs jump after 2022 mainly because the league grew from 8 to 10 teams (more matches). Average score per innings is the fairer measure: about **155 in 2008** versus roughly **175–185 in the 2023–2026 seasons**.
3. **Wankhede Stadium hosted the most matches (132)**, followed by Eden Gardens (77) and M Chinnaswamy Stadium (65).
4. **Mumbai Indians lead in wins (155).** Among the teams on the chart, Gujarat Titans have the highest win % (61.04% over 77 matches) and Chennai Super Kings lead the long-running franchises (55.85%).
5. **Player leaders:** V Kohli has the most runs (9,705) and YS Chahal the most wickets (233). CH Gayle leads the six-hitters (359).

---

## 🧹 Data Preparation (Power Query)

- Loaded Cricsheet JSON match files and flattened them into analysis-ready tables
- **Team Clean:** standardised franchise names so renamed teams are counted as one team
- **Venue Clean:** merged duplicate stadium names (for example the same ground written with and without the city) and shortened long labels
- Set data types, sorted the season field correctly, and removed fields not needed for the report

## 🧮 Data Model & DAX

Key measures used in the report:

| Measure | Purpose |
|---|---|
| Total Runs / Fours / Sixes / Matches | Headline KPIs |
| Avg Runs per Innings | Fair season-to-season scoring comparison |
| Win % | Wins divided by matches played, per team |
| Toss Win % by Decision | Match win rate for toss winners who chose to bat or field |
| Top Run Scorer / Top Wicket Taker | Dynamic cards that respond to the Season and Team slicers |

---

## 🎨 Design Choices

- 1280 × 720 canvas, consistent 15 px spacing between cards
- Segoe UI throughout, with a clear order: title, then KPI values, then visual titles, then labels
- Navy and blue palette with an orange accent, saved as a custom theme
- One page by design: the main story should be clear in about 10 seconds

---

## 📚 What I Learned

- Working with nested JSON match data and shaping it into analysis-ready tables
- Cleaning inconsistent team and venue names in Power Query
- Writing DAX measures that respond to slicers (win %, average score per innings, top scorer cards)
- Choosing the right metric: average score per innings instead of total runs, because the league grew from 8 to 10 teams
- Designing a clean one-page dashboard with a consistent theme and clear hierarchy

---

## 📁 Repository Structure

```
├── IPL_Dashboard.pbix      # Power BI report
├── images/
│   └── dashboard.png       # Dashboard screenshot
└── README.md
```

## ▶️ How to Open

1. Download `IPL_Dashboard.pbix`
2. Open it in **Power BI Desktop** (free)
3. Use the Season and Team slicers to explore

---

## 🚀 Future Improvements

- Team Analysis page (wins vs total runs, win % when batting first vs chasing)
- Venue-level analysis and over-wise scoring (powerplay vs death overs)
- Reset button and page navigation
- Player-level drill-through

---

## 🙋 About Me

Built by **Prathamesh Wadaskar**, a Computer Engineering graduate interested in Data Analytics, Business Intelligence and Data Visualization. I'm open to Data Analyst / BI Analyst roles.

If you find this project interesting, feel free to explore the repository and share your feedback.

- LinkedIn: https://www.linkedin.com/in/prathamesh-wadaskar/
- GitHub: https://github.com/Prathamesh8287

## 📄 Data Source

Ball-by-ball data from [Cricsheet](https://cricsheet.org/). Please refer to Cricsheet for its data terms and attribution requirements.
