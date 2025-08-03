# Brent Oil Price Event Analysis

## Project Overview

This project investigates how major geopolitical and economic events have influenced Brent crude oil prices between May 1987 and September 2022. By implementing Bayesian Change Point Detection using PyMC3, the objective is to identify structural shifts in oil price behavior and correlate them with real-world events such as wars, OPEC production decisions, economic sanctions, and financial crises.

## Business Objective

The project is designed to provide actionable insights for the following stakeholders:

- **Investors** – To better understand oil market volatility and improve investment decision-making.
- **Policymakers** – To evaluate the economic impact of geopolitical risks and inform energy security strategies.
- **Energy Companies** – To plan production, pricing, and hedging strategies with increased foresight.

## Situational Context

This analysis was conducted by a data scientist at **Birhan Energies**, a strategic analytics firm focused on the global energy market. The core task is to:

- Identify events that triggered significant shifts in Brent oil prices.
- Quantify and explain the magnitude of those impacts.
- Communicate findings to guide investments, policy formulation, and operations.

---

## Repository Structure

brent-oil-change-points/
│
├── data/                # Raw and processed datasets
│   ├── brent_oil_prices.csv
│   └── key_events.csv
│
├── notebooks/           # Exploratory analysis and modeling notebooks
│   ├── 01_eda_cleaning.ipynb
│   ├── 02_event_mapping.ipynb
│   └── 03_bayesian_model.ipynb
│
├── src/                 # Python modules (modeling, utils)
│   └── change_point_model.py
│
├── dashboard/           # Flask + React dashboard application
│   ├── backend/         # Flask APIs
│   └── frontend/        # React UI
│
├── reports/             # PDF/Markdown reports and visualizations
│   └── final_report.pdf
│
├── requirements.txt     # Python dependencies
└── README.md            # This file


---

## Project Tasks and Workflow

### Task 1: Data Analysis Foundation

- **Data Cleaning**  
  Removed 3,996 duplicate records and validated positive price entries. Aggregated daily data to monthly averages for better trend visibility.

- **Exploratory Data Analysis**  
  Conducted trend analysis using line plots, volatility visualization using rolling statistics, and seasonality decomposition using STL.

- **Stationarity Checks**  
  Used the Augmented Dickey-Fuller (ADF) test. Applied first-order differencing to make the series stationary, a prerequisite for time series modeling.

- **Event Dataset Compilation**  
  Compiled a structured dataset of 15+ major events affecting global oil markets between 1987 and 2022, with annotated start dates and contextual summaries.

- **Assumptions and Limitations**  
  Acknowledged that statistical correlations do not confirm causation. Accounted for lag effects, confounding factors, and data noise.

- **Communication Strategy**  
  Identified executive and technical stakeholders, defined deliverables (reports, dashboards, repository), and selected communication channels (email, GitHub, presentations).

### Task 2: Change Point Detection (Bayesian Modeling with PyMC3)

- **Model Design**  
  Built a Bayesian change point model with PyMC3 to estimate latent switch points and model mean oil price shifts before and after structural changes.

- **Inference**  
  Applied Markov Chain Monte Carlo (MCMC) to sample posterior distributions of mean prices and switch points.

- **Insights**  
  - Detected multiple structural breaks in oil prices.
  - Aligned statistical change points with real-world events such as the 2008 financial crisis, COVID-19, and OPEC+ decisions.
  - Quantified shifts in average prices across identified regimes.

- **Model Interpretation**  
  Illustrated uncertainty using trace plots and density curves. Clearly communicated probabilistic outcomes.

### Task 3: Interactive Dashboard

- **Features**  
  Developed an interactive dashboard to allow users to:
  - View historical oil price movements
  - Inspect detected change points
  - Overlay key geopolitical and economic events
  - Explore volatility metrics and average price shifts
  - Filter data by event type or time range

- **Technology Stack**  
  - **Backend**: Flask REST APIs
  - **Frontend**: React.js with Chart.js and Recharts for dynamic visualizations

---

## Technical Highlights

| Component            | Description                                      |
|---------------------|--------------------------------------------------|
| Modeling Framework  | PyMC3 with MCMC sampling                         |
| Statistical Approach| Bayesian Inference for change point detection    |
| Event Dataset       | Curated geopolitical and economic events (1987–2022) |
| Stationarity Tests  | ADF Test and differencing                        |
| Dashboard           | Flask API + React.js frontend                    |

---

## Data Description

**Brent Oil Price Dataset**
- **Fields**:
  - `Date` – Daily time stamps
  - `Price` – Brent crude price in USD/barrel

**Event Dataset**
- **Fields**:
  - `event_name` – Title of the geopolitical or economic event
  - `description` – Brief summary of the event
  - `start_date` – Approximate date the event began

---

## Key Insights

- Structural breaks in Brent oil prices strongly correlate with global financial shocks, political conflicts, and strategic OPEC policy shifts.
- The Bayesian framework offers robust probabilistic reasoning for detecting changes and communicating uncertainty.
- Major events such as the Iraq War, COVID-19 lockdowns, and 2022 Russia–Ukraine war align closely with identified change points.

---

## Installation and Setup

To run the project locally:

1. **Create a virtual environment**  
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

2. Install dependencies

   pip install -r requirements.txt
   
3. Run notebooks or launch the dashboard

   cd dashboard/backend
flask run


5. 
