# Task 1: Laying the Foundation for Brent Oil Price Analysis

## Project Context

This project involves analyzing historical Brent oil price data to understand underlying trends, seasonality, and structural changes driven by geopolitical, economic, and OPEC-related events. Task 1 establishes the foundational groundwork required for rigorous time series analysis and subsequent modeling.

---

## Dataset Overview

- **Source:** Historical Brent crude oil prices.
- **Period Covered:** May 20, 1987 – November 2022.
- **Data Fields:**
  - `Date`: Recorded date (converted to datetime format).
  - `Price`: Brent oil price in USD per barrel.
  
The raw dataset initially contained daily price entries with duplicate records and no datetime indexing. Data was processed and aggregated to monthly frequency for robust analysis.

---

## Task 1: Completed Activities

### 1. Data Cleaning and Preprocessing

- Loaded the raw dataset and inspected for quality issues.
- Removed 3996 duplicate records, reducing the dataset size from 9011 to 5015 entries.
- Verified zero missing values across all columns.
- Confirmed that all `Price` entries are positive with no erroneous or zero values.
- Aggregated data to a monthly frequency by computing the mean price per month.
- Set the `Date` column as a datetime index for time series consistency.

### 2. Exploratory Data Analysis (EDA)

- Visualized Brent oil prices over time using line plots to identify trends and fluctuations.
- Created histograms and boxplots to analyze the distribution of prices and detect potential outliers (none found).
- Computed and plotted rolling statistics (rolling mean and rolling standard deviation) with window sizes of 12 months to observe trends and volatility changes.
- Performed seasonal decomposition using additive models to isolate trend, seasonal, and residual components — revealing clear long-term trends and seasonal patterns.

### 3. Time Series Stationarity Analysis

- Conducted Augmented Dickey-Fuller (ADF) tests on the original series, indicating non-stationarity (p-value > 0.05).
- Applied first-order differencing to remove trend effects, resulting in a stationary series (p-value ≪ 0.05).
- Confirmed stationarity is essential to avoid spurious results in time series modeling.

### 4. Definition of Data Analysis Workflow

Outlined a comprehensive workflow for the project, including:

- Data cleaning and transformation steps.
- Exploratory data analysis and visualization.
- Stationarity and seasonality assessment.
- Compilation of external event data to contextualize price movements.
- Modeling strategy focusing on change point detection and time series forecasting.
- Communication plan for stakeholder deliverables.

### 5. Compilation of Key Event Data

- Researched and compiled a structured dataset of approximately 15 major geopolitical events, OPEC meetings, and economic shocks impacting the oil market.
- The events dataset contains event names, descriptions, and approximate start dates to be used for correlational and causal analysis.

### 6. Assumptions and Limitations

- Explicitly noted that statistical correlation in time series does not imply causation.
- Acknowledged limitations such as potential confounding variables, data aggregation effects, and measurement errors.
- Emphasized the importance of domain knowledge when interpreting structural changes and price fluctuations.

### 7. Media and Communication Strategy

- Determined key formats for communicating insights:
  - Interactive dashboards for real-time data exploration.
  - Detailed analytical reports documenting methodology and findings.
  - Visual presentations for executive stakeholders.
- Identified main channels for dissemination: internal project repositories, email briefings, and virtual presentations.

---

## Next Steps

- Implement and apply change point detection algorithms to identify structural breaks in the Brent oil price time series.
- Investigate the temporal alignment of detected change points with compiled geopolitical and economic events.
- Refine seasonality models and explore other smoothing techniques to better capture cyclical behaviors.
- Prepare for advanced time series forecasting leveraging insights from stationarity and structural break analyses.

---

## Repository Structure

/task-1
│

├── docs/

│ └── (supporting documentation and references)

│

├── notebooks/

│ ├── task1_data_cleaning_and_eda.ipynb # Initial data cleaning, EDA, and stationarity tests

│ ├── task1_analysis.ipynb # Detailed analysis workflows and modeling prep

│ └── event_data_creation.ipynb # Research and compilation of oil market event data

│

├── data/

│ ├── brent_oil_prices.csv # Original raw daily Brent oil price data

│ ├── cleaned_brent_oil_prices.csv # Cleaned and aggregated monthly price data

│ └── oil_market_events.csv # Structured dataset of key geopolitical/economic oil market events

│

├── reports/

│ └── data_analysis_workflow.md # Detailed description of the data analysis workflow, assumptions, and communication strategy

│

└── README.md # This file, summarizing Task 1 progress and structure