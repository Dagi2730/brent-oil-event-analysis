Assumptions
1. Data Accuracy and Completeness
The Brent oil price dataset used in this analysis is assumed to be accurate and comprehensive, representing daily market prices from May 20, 1987, to September 30, 2022.

It is assumed that there are no significant measurement errors, missing values, or reporting biases affecting the price data.

2. Event Dates and Impact
The dates associated with geopolitical, economic, and OPEC events are approximate and based on publicly available information.

The analysis assumes that these dates correspond closely to the timing when these events began to influence oil prices.

It is also assumed that the market reaction to these events occurs within a reasonable timeframe around these dates.

3. Market Reaction Mechanism
The oil market prices are assumed to respond primarily to the compiled major events.

This analysis assumes that these events have a meaningful and detectable impact on the price movements within the time series.

4. Stationarity of Differenced Series
After differencing the price series to remove trends, the resulting series is assumed to be stationary.

Stationarity is an important assumption for many time series modeling techniques used later in the project.

5. Exclusion of Other Factors
The analysis assumes no major omitted variables or unobserved confounders that might have substantial impacts on oil prices outside of the included event dataset.

Limitations
1. Distinguishing Correlation from Causation
While the analysis can identify statistical correlations between oil prices and key events, it cannot prove causal relationships.

Multiple external factors, including market speculation, policy changes, supply-demand imbalances, and other macroeconomic variables, may simultaneously influence prices.

Establishing causality requires more complex experimental or econometric designs not covered in this analysis.

2. Event Selection and Coverage Bias
The list of events compiled is limited to major, well-documented geopolitical, economic, and OPEC decisions.

Some relevant regional, minor, or less publicized events may be excluded, potentially biasing the analysis.

The timing and impact magnitude of events can vary widely and are often uncertain.

3. Data Granularity and Timing Mismatches
The dataset contains daily prices, which may mask intra-day volatility or very short-lived shocks.

The exact market reaction to events may lead or lag the recorded event date, causing potential misalignment.

Additionally, not all price changes can be directly linked to known events due to market complexity.

4. Modeling Assumptions
Time series analyses, including stationarity tests and change point detection, rely on assumptions (e.g., stationarity, linearity, independence) that may not fully hold in real market data.

These assumptions can limit the accuracy and generalizability of model conclusions.

5. Lack of Additional Market Data
The analysis focuses exclusively on price data without incorporating other relevant market variables such as trading volumes, production levels, inventories, or demand statistics.

The absence of these data restricts the scope of insights and limits understanding of price drivers.

