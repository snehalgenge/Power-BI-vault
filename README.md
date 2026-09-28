# Power-BI-vault
End-to-end Business Intelligence dashboards showcasing complex data modeling, interactive layouts, and scalable analytical solutions. , An active storage hub for interactive data visualizations, creative UI/UX reporting, and analytical data stories.
# ASIA CUP (1984–2023): THE CONTINENTAL LEDGER

An enterprise-grade sports intelligence dashboard tracking **39 years of cricket history** across the Asian subcontinent [f]. **"The Continental Ledger"** serves as the definitive balance sheet of the Asia Cup, meticulously auditing every run scored, wicket taken, and match outcome from the inaugural 1984 tournament in Sharjah to the 2023 championship [f].

---

## 📊 Dashboard Architecture & Layout

This analytical report is engineered across **3 functional pages**, featuring fluid **Page Navigation (Back & Forward buttons)** to ensure seamless user exploration [f].

### 📌 Page 1: The Continental Ledger (Historical Overview)
This page functions as the macro-level audit of the tournament's history [f].

*   **6 Core KPIs (Key Performance Indicators):**
    *   **Total Matches** - Aggregate games played across all tournament editions [f].
    *   **Total Runs** - Cumulative runs accumulated in tournament history [f].
    *   **Total Wickets** - Aggregate bowling dismissals recorded [f].
    *   **Batting Average** - Overall runs scored per wicket lost [f].
    *   **Tournament Run Rate** - Global scoring velocity per over [f].
    *   **Total Centuries** - Total individual triple-digit scores [f].
*   **Interactive Controls & Slicers:**
    *   **Year Slicer** - Multi-select filter to isolate specific editions or decades [f].
    *   **Opponent Team Slicer** - Dynamic filter to evaluate match performance against specific nations [f].
    *   **Result Filter** - Toggle criteria between Wins, Losses, Ties, or No-Results [f].
*   **Visualizations:**
    *   **Team-Wise Total Matches** - Bar chart breaking down historical participation and volume of games played by country [f].
    *   **Section-Wise Match Win Dropdown** - Deep-dive matrix filtered by a Team Dropdown to isolate specific era/stage performance metrics [f].
    *   **Total Win Gauge** - Data dial showcasing absolute win milestones against historical performance benchmarks [f].

---

### 📌 Page 2: Legend Analytics (Player & Team KPI Spotlights)
A deep-dive page focused heavily on elite individual milestones, boundaries, and team discipline profiles [f].

*   **Player Analytics Matrix:**
    *   **Top 20 Players by Player of the Match (POM)** - Ranked leaderboard showcasing the most impactful continental match-winners [f].
    *   **Individual Wickets Leaderboard** - Tracking the tournament's premium historical bowlers [f].
*   **Team Statistical Breakdowns:**
    *   **Total Runs & Strike Rate** - Dual-axis visualization comparing high-volume scoring against team scoring velocity [f].
    *   **Boundary Audits** - Team-wise aggregate distribution of total 4s and 6s smashed [f].
    *   **Wicket Balance Sheet** - Structural contrast metric tracking **Wickets Taken vs. Wickets Lost** by team [f].
*   **Geographical Dynamics:**
    *   **Team Location-Wise Result** - Geospatial/matrix visual showcasing how teams perform based on host nation/venue conditions [f].

---

### 📌 Page 3: The Arch-Rivalry Ledger (India vs. Pakistan Focus)
An exact structural replica of Page 1, hard-filtered to isolate cricket's greatest historic rivalry [f].

*   **Page-Level Hard Filters:** Data rows are strictly locked to **India** and **Pakistan** match history [f].
*   **Executive Summary Box:** A high-level qualitative and quantitative commentary window highlighting head-to-head title splits, historical dominance eras, and critical win-loss margins [f].
*   **Replicated Architecture:** Echoes the 6 KPIs, Team Matches, Match Win Dropdowns, and Win Gauges from Page 1 to allow direct, uncluttered comparative analysis between the two giants [f].

---

## 🧮 Data Modeling & DAX Measures

The intelligence of this ledger relies on clean, fundamental **Data Analysis Expressions (DAX)** to dynamically compute performance realities. Below are the core measures written for this project:

```dax
// 1. Total Matches Played
Total Matches = COUNTROWS('AsiaCup_Matches')

// 2. Total Runs Scored
Total Runs = SUM('AsiaCup_Stats'[Runs])

// 3. Total Wickets Taken
Total Wickets = SUM('AsiaCup_Stats'[Wickets])

// 4. Total Matches Won (For Gauges and Dropdowns)
Total Wins = CALCULATE(
    COUNTROWS('AsiaCup_Matches'), 
    'AsiaCup_Matches'[Result] = "Won"
)

// 5. Total Boundaries (4s)
Total 4s = SUM('AsiaCup_Stats'[Fours])

// 6. Total Boundaries (6s)
Total 6s = SUM('AsiaCup_Stats'[Sixes])
```

---

## 🛠️ Tech Stack & Implementation Details

*   **Business Intelligence / Data Viz:** Power BI Desktop [f]
*   **Data Modeling & Transformations:** DAX / Power Query [f]
*   **Navigation Feature:** Native Bookmark and Action buttons utilized to map out **Forward (➔)** and **Back (⬅)** user journey flows [f].
