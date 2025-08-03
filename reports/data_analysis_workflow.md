# 📊 Data Analysis Workflow – Brent Oil Price Project

## Objective:
Analyze historical Brent crude oil prices to identify structural changes and understand how major geopolitical/economic events impact oil price behavior.

---

## 1. 🧠 Data Understanding

- Review the structure and size of the Brent oil dataset.
- Identify the data types for each column.
- Understand time granularity (daily, monthly?).
- Identify the range of dates available.
- Verify if it includes additional features like volume or indicators (if any).

---

## 2. 🧹 Data Cleaning & Preprocessing

- Convert date column to datetime format and set it as index.
- Sort data chronologically.
- Check for:
  - Missing values (and handle appropriately).
  - Duplicates (drop if needed).
  - Negative or zero prices (flag as potential errors).
- Handle outliers (visual inspection or IQR-based filtering).
- Confirm no gaps in the time series (missing business days or months).

---

## 3. 📈 Exploratory Data Analysis (EDA)

- **Trend analysis:**
  - Plot the time series to understand overall movement.
  - Use rolling means to smooth and detect underlying trends.

- **Seasonality/Cycles:**
  - Decompose the time series into trend, seasonality, and residuals.
  - Compare yearly/monthly patterns (if applicable).

- **Distribution & Summary:**
  - Histogram and KDE of prices.
  - Summary statistics (mean, median, variance, etc.)

- **Volatility:**
  - Use rolling standard deviation to detect high-volatility periods.
  - Plot percentage price changes (daily returns).

---

## 4. 🗓️ Event Data Compilation

- Research and compile a structured CSV of major global events affecting oil prices (e.g., wars, pandemics, OPEC decisions).
- Structure: `date,event,category,description`
- This will later be merged or annotated with the price data to explain significant change points.

---

## 5. 📉 Stationarity & Transformation

- Apply Augmented Dickey-Fuller (ADF) Test to check for stationarity.
- Apply differencing or log transformation to stabilize variance or trend if necessary.
- Visualize transformed series to confirm improvements.

---

## 6. 📌 Change Point Detection

- Use change point detection algorithms (e.g., `ruptures`, `prophet changepoints`) to identify moments of structural change.
- Visualize changepoints overlaid on price time series.
- Try to align changepoints with known events from your event CSV.

---

## 7. 🤖 Modeling (Later in Task 2)

- Use ARIMA/Prophet for forecasting future prices.
- Segment time series into pre/post-changepoint intervals for analysis.
- Compare model performance across periods.
- Predict impact of future hypothetical events on prices.

---

## 8. 💡 Insights & Interpretation

- Analyze changes in oil price behavior across historical periods.
- Identify what types of events lead to largest changes (economic vs war vs OPEC policy).
- Identify stable vs volatile regimes.

---

## 9. 📢 Communication & Reporting

- **Dashboards:**
  - Interactive dashboards using Streamlit or Plotly Dash for stakeholders.

- **Report:**
  - Well-structured final report (PDF, Google Docs, or Notion) including:
    - Plots
    - Model outputs
    - Explanations
    - Recommendations

- **Presentation:**
  - Slide deck summarizing key findings and visual storytelling for non-technical stakeholders.

---

## Deliverables Summary:

| Step | Output |
|------|--------|
| Data Cleaning | Cleaned DataFrame with no nulls/outliers |
| EDA | Visuals (trend, seasonality, distribution) |
| Events | CSV of major events affecting oil |
| Changepoints | Detected breakpoints with explanation |
| Report | Final report and/or dashboard |

---

