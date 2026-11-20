# Airline Flight Delay & On-Time Performance Analysis

**Project 14 | Industry:** Aviation / Transportation  
A beginner-friendly exploratory data analysis project using Python, NumPy, Pandas, and Matplotlib.

## Project overview
Analyze flight records to understand departure/arrival delays, origin-airport performance, worst routes, time-of-day patterns, delay causes, cancellations, diversions, correlation, statistical distributions, and delay outliers.

## Dataset
`data/14_flight_delays.csv` — supplied teaching dataset. Original file has **913 rows and 11 columns**. After removing duplicate `Flight_ID` entries, the analysis has **900 records**. The dataset is synthetic/educational; findings are not real-world aviation statistics.

## Project tasks
1. Load and inspect CSV, columns, shape, and data types.
2. Check missing values and duplicate flight IDs.
3. Handle missing arrival delays (median imputation for descriptive summaries).
4. Convert date and extract month/day of week.
5. Calculate flight count, average departure delay, and on-time percentage (departure delay <= 15 min).
6. Rank airports by average departure delay.
7. Find 10 routes with highest average arrival delay.
8. Compare delay rates across Morning/Afternoon/Evening/Night.
9. Analyze delay causes, reporting missing cause values separately.
10. Airline cancellation/diversion percentages.
11. Correlation of departure and arrival delays (complete original pairs only).
12. NumPy median, standard deviation, and 90th percentile.
13. IQR outlier detection.
14. Delay severity categories.
15. Five operational recommendations.

## Repository structure
```text
SRS/project_SRS.docx
src/airline_flight_delay_analysis.ipynb
data/14_flight_delays.csv
README.md
requirements.txt
```

## Setup and run
1. Install Python 3.9+.
2. Clone/download this repository.
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Open notebook:
   ```bash
   jupyter notebook src/airline_flight_delay_analysis.ipynb
   ```
5. Run all cells in order. If the notebook is launched from a different working directory, its CSV path fallback tries the repository-root data path.

## Data decisions
- Duplicate `Flight_ID`: keep the first record.
- Missing `Arrival_Delay_Mins`: median imputation for descriptive summaries.
- Missing `Delay_Cause`: preserve and show as Unknown/Missing.
- `Departure_Time` is already categorical (Morning/Afternoon/Evening/Night); it is grouped as-is.
- Correlation uses only originally non-missing arrival-delay records.
- IQR outliers and same-origin/destination routes are flagged, not automatically removed.
- Delay severity thresholds are documented in the notebook.

## Expected outputs
- Airport delay ranking table and graph
- Top 10 route delay table and graph
- Time-of-day comparison
- Delay-cause breakdown
- Airline cancellation/diversion table
- Correlation and NumPy statistics
- Outlier table and delay-severity chart
- Five recommendations

## Limitations
Synthetic dataset; limited sample; missing delay-cause values; imputation can affect descriptive statistics; correlation does not prove causation; unusual same-airport routes need verification.

## Author
Student project — update this section with your name and Student ID before submission.
