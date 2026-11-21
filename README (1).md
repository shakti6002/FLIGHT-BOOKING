# ✈️ Flight Ticket Price Analysis

## 📌 Project Overview
This project explores airline flight booking data to understand ticket price patterns and how prices relate to travel distance, booking lead time, travel class, booking channel, airline type, and source city.

The notebook also performs data cleaning, handles missing values and invalid passenger ages, and creates price categories for further analysis.

## 🎯 Objectives
- Inspect the dataset structure, size, and summary statistics.
- Identify missing values and duplicate records.
- Clean the data by removing duplicates and filling missing values.
- Check and correct invalid values (such as passenger ages outside 0–100).
- Explore ticket-price distribution and summary statistics.
- Study the relationship between ticket price, distance, and days before departure.
- Compare average ticket prices across source cities, travel classes, booking channels, and airline types.
- Categorize bookings as **Budget**, **Regular**, or **High-Value**.

## 🧰 Tools & Libraries
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

## 📊 Analysis Performed
### 1. Data Inspection
- Dataset shape and column information
- Preview of first and last records
- Descriptive statistics
- Missing-value and duplicate checks

### 2. Data Cleaning
- Removed duplicate rows
- Filled missing `Booking_Channel` values with the mode
- Filled missing `Days_Before_Departure`, `Passenger_Age`, and `Baggage_Kg` values with their medians
- Replaced passenger ages outside the 0–100 range with the median age
- Checked for invalid values in distance, booking lead time, passenger age, baggage, and ticket price

### 3. Exploratory Data Analysis (EDA)
- Ticket price summary statistics
- Ticket price distribution histogram
- Correlation between distance, booking lead time, and ticket price
- Scatter plots:
  - Distance vs. Ticket Price
  - Days Before Departure vs. Ticket Price

### 4. Category Comparisons
Average ticket prices are compared by:
- Source City
- Travel Class
- Booking Channel
- Airline Type

### 5. Price Segmentation
Ticket prices are grouped using the following rules:
- **Budget:** Price below ₹2,500
- **Regular:** Price from ₹2,500 to ₹6,000 (inclusive)
- **High-Value:** Price above ₹6,000

A count plot is used to visualize the number of bookings in each price category, and selected characteristics of Budget and High-Value bookings are compared.

## 📁 Project Structure
```text
project/
├── data/
│   └── raw/
│       └── flight_data.csv
├── notebooks/
│   └── draft1.ipynb
└── README.md
```

> The notebook currently reads the dataset from `../data/raw/flight_data.csv`. Keep the dataset in the expected location relative to the notebook, or update the file path in the notebook before running it.

## ▶️ How to Run
1. Clone or download this project.
2. Make sure Python and Jupyter Notebook are installed.
3. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
4. Place `flight_data.csv` in `data/raw/`.
5. Open the notebook:
   ```bash
   jupyter notebook
   ```
6. Open `draft1.ipynb` and run the cells from top to bottom.

## 💾 Output
The notebook exports the cleaned dataset, including the `Price_Category` column, to:
```text
flight_analysis_final.csv
```

## 📌 Notes
- This notebook is an exploratory data analysis project; it does not build a machine-learning prediction model.
- The dataset is required to execute the notebook. It is not included in this repository unless added separately.

## 👤 Author
**Your Name**
