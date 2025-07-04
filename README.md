# P153112-STQD6324-ASGMT2
Analysis of flight delays and cancellations using Hive, HDFS, and Python (Colab)

# Airline On-Time Performance Analysis (2006)

Have you ever been stuck at an airport due to a delayed or cancelled flight and wondered if someone could’ve predicted it? This project explores that possibility using the *Airline On-Time Performance* dataset.

## Project Overview
This analysis dives into the 2006 flight records from the [Airline On-Time Performance](https://tinyurl.com/u8rzvdsx) dataset (Kaggle), with the goal to analyse when and why delays and cancellations happen and which routes and carriers are the most problematic.

---

## Workflow Summary

| Stage                    | Tool Used        | Description                                              |
|--------------------------|------------------|----------------------------------------------------------|
| Virtualization           | Oracle VM        | Run Ambari Sandbox (HDP 2.6.5) for Hive queries          |
| Data Cleaning & Prep     | Hive + HDFS      | Run queries using `hive -e` and store output in HDFS     |
| File Export              | PuTTY + WinSCP   | Export cleaned CSVs from HDFS to local machine           |
| Final Analysis           | Google Colab     | Perform data analysis, visualization, and interpretation |

---

## ✅ Questions Answered

### 1. Delay Patterns
- **Time of Day**: Morning flights (especially before 9am) tend to have the lowest average delays.
- **Day of Week**: Tuesdays and Saturdays show better on-time performance.
- **Month/Season**: April, May, and September have higher on-time percentages with lower average delays. Summer (June, July) and winter (December) experience more delays due to peak travel and weather issues.

### 2. Delay Factors
- **Top Contributors**: Late Aircraft (37%), NAS (29%), and Carrier delays (28%) make up the bulk of delay minutes.
- **Quantified Impact**: See bar and pie charts for delay distribution in minutes and percentage.

### 3. Cancellations
- **Main Reasons**: Weather is a big contributor in early months; carrier-related cancellations are consistent throughout the year.
- **Overlay View**: Stacked bar chart + scheduled flights line chart help contextualize monthly spikes.
- **Q3.2 Output**: The analysis on whether cancellations correlate with specific airlines, airports, or time periods is based on an interactive map and seasonal bar chart. Since GitHub does not support interactive plots, a PNG snapshot of the output has been included in the repo at
/plot_output/Q32_map_correlation.png for reference.

### 4. Problematic Routes
- Routes like ASE–ORD (OO), ALB–JFK (OH), and SEA–HNL (UA) show repeated issues.
- Most delays are linked to controllable factors like aircraft scheduling or carrier ops.
- Delay breakdown stacked bar chart shows clear patterns per route.

---

## 📁 File Structure
```bash
.
├── README.md
├── plot_output/
│   ├── Q11_lowest_delays.png
│   ├── Q12_ontime.png
│   ├── Q13_months_ontime.png
│   └── ... (per-question plot outputs)
├── colab_notebooks/
│   ├── airline_analysis_2006.ipynb
```

---

## Highlights
- Used real-world data (7M+ rows) for practical analysis
- Multi-tool pipeline: Hive + Linux shell + Colab + seaborn/Matplotlib
- Clean, insightful plots tied directly to real performance issues

---

## Future Work
- Extend to other years (2007–2008)
- Add machine learning models to predict delays
- Integrate real-time weather and ATC data for more accurate forecasting

---

Feel free to clone this repo, explore the notebooks, and build your own insights. Contributions are welcome!

> **Created by Afiqah Khairuna @ Universiti Kebangsaan Malaysia**

