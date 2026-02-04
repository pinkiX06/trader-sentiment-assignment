# Trader Performance vs Market Sentiment

## Objective
Analyze how market sentiment (Fear/Greed) relates to trader behavior and performance on Hyperliquid.  
The goal is to understand how sentiment impacts profitability, trading activity, and risk behavior, and to derive actionable strategy insights.

## Datasets
- fear_greed_index.csv: Bitcoin market sentiment data (Fear/Greed classification by date)
- historical_data.csv: Historical trader data from Hyperliquid (trades, PnL, size, side, etc.)

## Project Structure
- assignment.ipynb : Main analysis notebook
- data/ : Contains the datasets
- outputs/ : Contains generated charts and figures
- README.md : Project description and instructions

## Setup

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn

## How to Run

Open assignment.ipynb in Jupyter Notebook or VS Code.

Make sure the data/ folder contains:
- fear_greed_index.csv
- historical_data.csv

Run all cells from top to bottom.

The notebook will:
- Clean and prepare the data
- Merge datasets by date
- Generate analysis tables and charts
- (Bonus) Train a simple predictive model


## Methodology (Summary)

Loaded and inspected both datasets (shape, missing values, duplicates).  
Converted timestamps and aligned both datasets at daily level using a common date column.  
Merged trader data with market sentiment data on date.  
Created key metrics:
- Daily PnL per account
- Win rate
- Trade frequency
- Average trade size

Compared performance and behavior between Fear and Greed days.  
Segmented traders (e.g., frequent vs infrequent, high vs low PnL).  
(Bonus) Built a simple machine learning model to predict trade profitability using sentiment and trade features.


## Key Insights

- Trading performance (PnL and win rate) differs between Fear and Greed days.
- Trader behavior changes with sentiment, especially in terms of trade frequency and position size.
- Frequent traders and infrequent traders show different performance patterns across sentiment regimes.


## Strategy Recommendations (Part C)

- On Fear days, reduce risk by lowering position size and trade frequency, as performance tends to be weaker.
- On Greed days, allow higher activity for consistently performing traders, while keeping risk controls for others.
- Use market sentiment as a simple risk filter in trading strategies (aggressive mode on Greed days, conservative mode on Fear days).


## Bonus

Implemented a simple Random Forest model to predict whether a trade will be profitable using:
- Market sentiment (encoded)
- Trade size
- Trade direction 

This shows that sentiment and basic behavior features contain predictive signal and can be used for risk management or trade filtering.

