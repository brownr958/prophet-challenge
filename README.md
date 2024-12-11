# Mercado Libre Data Analysis with Prophet

## Overview
This project involves analyzing financial and user data for Mercado Libre, the most popular e-commerce site in Latin America. The goal is to explore search traffic data, uncover patterns, and model trends to support business decisions. The analysis follows a structured four-step approach and leverages the Prophet library for time-series forecasting.

## Steps Completed

### Step 1: Find Unusual Patterns in Hourly Google Search Traffic
- **Data Preparation:** Loaded Google search traffic data into a DataFrame.
- **Analysis:** Sliced the data to May 2020 and visualized unusual patterns.
- **Comparison:** Calculated total search traffic for May 2020 and compared it to the monthly median.
- **Insights:** Assessed whether the increase in search traffic correlated with the release of financial results.

### Step 2: Mine the Search Traffic Data for Seasonality
- **Hourly Trends:** Grouped data by hour of the day and plotted average traffic.
- **Weekly Trends:** Grouped data by the day of the week to identify peaks.
- **Seasonal Trends:** Grouped data by week of the year to analyze patterns.
- **Insights:** Observed time-based trends in search traffic to optimize marketing ROI.

### Step 3: Relate the Search Traffic to Stock Price Patterns
- **Data Integration:** Combined stock price data with search traffic data into a single DataFrame.
- **Temporal Analysis:** Sliced the dataset to the first half of 2020 and analyzed trends.
- **Feature Engineering:**
  - Created a `Lagged Search Trends` column by shifting search data by one hour.
  - Computed `Stock Volatility` as an exponentially weighted rolling average.
  - Calculated `Hourly Stock Return` as the percent change in stock prices.
- **Insights:** Evaluated relationships between search traffic, volatility, and returns.

### Step 4: Create a Time Series Model with Prophet
- **Data Preparation:** Prepared search traffic data for Prophet modeling.
- **Model Training:** Trained a Prophet model to forecast future trends.
- **Visualization:**
  - Plotted forecast results.
  - Analyzed individual components such as trends and seasonality.
- **Insights:** Answered questions about time-of-day, day-of-week, and yearly patterns.

## Tools Used
- **Python Libraries:** pandas, matplotlib, Prophet
- **Notebook Environment:** Google Colab

## Key Files
- `forecasting_net_prophet.ipynb`: The Jupyter Notebook containing all analysis and code.
- `prophet_model.pkl`: Serialized Prophet model for forecasting.

## How to Use
1. **Clone the Repository:**
   ```bash
   git clone <repository_url>
   cd prophet-challenge
   ```
2. **Install Dependencies:** Ensure the required Python libraries are installed:
   ```bash
   pip install pandas matplotlib prophet
   ```
3. **Run the Notebook:** Open the Jupyter Notebook file in Google Colab or locally:
   ```bash
   jupyter notebook forecasting_net_prophet.ipynb
   ```
4. **Review Outputs:** Execute the notebook cells sequentially to reproduce the analysis.

## Insights and Business Implications
- **Search Traffic Patterns:** Identified specific times of day and days of the week with peak search traffic.
- **Stock Price Relationship:** Found correlations between lagged search traffic, stock volatility, and returns.
- **Forecasting:** Provided actionable insights into future search traffic trends, aiding marketing and financial strategies.

## Author
Ryan
