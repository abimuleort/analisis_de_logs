# 📊 Server Log Analysis

A data analysis project built in Python using a Jupyter Notebook. It processes server log data from a CSV file to identify patterns, detect critical moments, and visualize system behavior over time.

---

## 🔍 What It Does

The notebook performs a full analysis pipeline on server logs, including:

- **Severity and status classification** — boolean columns to flag critical and failed events
- **Time-window binning** — groups events into 5-minute intervals using `dt.floor('5min')` for trend analysis
- **Critical moment detection** — identifies time windows with unusually high error rates compared to a baseline
- **Baseline comparison tables** — contrasts normal vs. anomalous periods
- **Visualizations** — matplotlib charts showing event distribution and spike detection over time

---

## 🛠️ Technologies

- **Python 3**
- **pandas** — data loading, transformation, and time-based grouping
- **matplotlib** — charts and timeline visualizations
- **SQLite** — querying and storing structured log data
- **Jupyter Notebook** — interactive analysis environment

---

## ▶️ How to Run

Install the required libraries:

```bash
pip install pandas matplotlib
```

Then open the notebook:

```bash
jupyter notebook analisis.ipynb
```

Run the cells in order from top to bottom.

---

## 📁 Project Structure

```
log_analysis/
├── analisis.ipynb     # Main analysis notebook
├── server_logs.csv    # Input dataset with server log entries
└── venv/              # Virtual environment (not tracked)
```

---

## 📌 Notes

- The dataset (`server_logs.csv`) contains timestamped server events with severity levels and HTTP status codes.
- Time binning uses `dt.floor('5min')` to group events into fixed windows for consistent trend comparison.
- Critical moments are flagged when a time window's error rate significantly exceeds the baseline average.

---

*Project developed as part of the Penguin Academy data analysis curriculum.*
