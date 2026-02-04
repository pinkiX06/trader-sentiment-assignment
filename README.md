# Trader Performance vs Market Sentiment

## Objective
Analyze how market sentiment (Fear/Greed) relates to trader behavior and performance on Hyperliquid.  
The goal is to understand how sentiment impacts profitability, trading activity, and risk behavior, and to derive actionable strategy insights.

## Datasets
- fear_greed_index.csv: Bitcoin market sentiment data (Fear/Greed classification by date)
- historical_data.csv: Historical trader data from Hyperliquid (trades, PnL, size, side, etc.)

## Project Structure
- analysis.ipynb : Main analysis notebook
- data/ : Contains the datasets
- outputs/ : Contains generated charts and figures
- README.md : Project description and instructions

## Setup

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
