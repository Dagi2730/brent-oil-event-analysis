# Brent Oil Price Event Analysis

## Project Overview

This project analyzes how major geopolitical and economic events impact Brent crude oil prices from May 1987 to September 2022. Using Bayesian Change Point modeling with PyMC3, the goal is to identify significant structural breaks in price behavior and link them to real-world events such as political decisions, conflicts, sanctions, and OPEC policies.

The insights will help investors, policymakers, and energy companies better understand market volatility, manage risks, and make informed decisions.

## Project Structure

- `data/` - Contains raw and processed datasets (Brent oil prices, key events)  
- `notebooks/` - Jupyter notebooks for exploratory data analysis and modeling  
- `src/` - Python modules for modeling and utility functions  
- `dashboard/` - Flask backend and React frontend for interactive visualization  
- `reports/` - Generated reports and visual assets  
- `requirements.txt` - Project Python dependencies  

## Setup Instructions

1. Create and activate a Python virtual environment:  
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate

2. Install dependencies:

    pip install -r requirements.txt

3. Launch Jupyter notebooks for analysis or run scripts in src/

Key Objectives

Detect change points in Brent oil prices with Bayesian models.

Correlate price changes with major geopolitical and economic events.

Provide actionable insights through reports and an interactive dashboard.
