# Forecasting Net Prophet

## Overview
This project analyzes financial and user data for MercadoLibre, the most popular e-commerce site in Latin America with over 200 million users. The goal is to find patterns in Google search traffic and determine if these patterns correlate with financial events and stock price movements, potentially enabling better stock trading decisions.
(NOTE: this work is for Educational purposes only - for "Project 8" (DU AI Bootcamp))

## Project Structure
The analysis is divided into four key steps:

### 1. Finding Unusual Patterns in Hourly Google Search Traffic
- Analyzing search data from May 2020 when MercadoLibre released quarterly financial results
- Comparing monthly search traffic against median values to identify anomalies
- Findings: Search traffic showed a slight increase (1.08%) during the financial results announcement period

### 2. Mining Search Traffic Data for Seasonality
- Analyzing hourly, daily, and weekly search patterns
- Key findings:
  - Search traffic peaks between 11 PM and 1 AM
  - Monday shows the highest search traffic, followed by Tuesday, with a gradual decline through the week
  - Search traffic shows noticeable dips during Latin American holidays and year-end holidays

### 3. Relating Search Traffic to Stock Price Patterns
- Concatenating stock price data with search traffic data
- Analyzing first half of 2020 (COVID-19 impact period)
- Creating metrics including lagged search trends, stock volatility, and hourly stock returns
- Key finding: Weak correlation between lagged search trends and stock volatility (-0.148), suggesting search traffic alone is not a strong predictor of stock performance

### 4. Creating a Time Series Model with Prophet
- Using Facebook's Prophet model to forecast future search traffic
- Analyzing time series components to identify:
  - Peak search times (late night/early morning)
  - Busiest days (Mondays)
  - Lowest search periods (December 24-31)
- Overall forecast shows stable patterns with slight growth potential

## Technologies Used
- Python
- Pandas
- Prophet (Facebook's forecasting tool)
- Matplotlib
- NumPy
- Datetime

## Installation
```bash
# Install required libraries
pip install pandas prophet numpy matplotlib
# Reference '.gitignore' file (for Python) as needed
```

## Usage
The Jupyter notebook contains all analysis with detailed comments. To run the analysis:
1. Clone this repository
2. Install dependencies
3. Run the Jupyter notebook

## Data Sources
- Google hourly search trends data for MercadoLibre
- MercadoLibre stock price data

## Conclusions
1) The analysis reveals that while there are clear temporal patterns in search traffic (time of day, day of week, and seasonal), these patterns have limited correlation with stock price movements. The Prophet model provides a stable forecast for future search trends, showing slight growth potential.
2) The lowest search traffic consistently occurs during year-end holidays, particularly between Christmas and New Year's, with December 24, 2018 showing the lowest recorded search volume.

## License
MIT license - copyright R_Stover for Educational purposes only

## Contributors
R_Stover - sole contributor for "Project 8" (DU AI Bootcamp)
