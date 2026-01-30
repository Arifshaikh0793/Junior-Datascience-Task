# Junior-Datascience-Task
# Trader Behavior vs Market Sentiment Analysis

## Assignment Overview

This project analyzes the relationship between trader performance and Bitcoin market sentiment (Fear vs Greed) using two datasets:

## 1)Bitcoin Market Sentiment Dataset
Columns: Date, Classification (Fear/Greed)
Represents overall market psychology.

## 2)Historical Trader Data from Hyperliquid
Includes fields such as account, symbol, execution price, size, side, time, start position, event, closedPnL, leverage, etc.
Represents real trader activity and performance.

## Objective of the Task

The goal of this project is to:

Explore how trader behavior changes under Fear vs Greed market conditions

Identify hidden behavioral patterns

Analyze trader profitability, risk, and volume

Derive insights that can support smarter trading strategies

This combines data science, behavioral finance, and trading analytics.

## What Was Done in This Project

Data Preparation

Cleaned both datasets

Standardized date formats

Merged trader data with market sentiment using Date

Handled missing values

Converted financial columns to numeric

Feature Engineering

## Key performance indicators were created:

abs_size_usd as a trade volume proxy

abs_start_position as a risk exposure proxy

is_profit as a profitable trade indicator

win_rate as the percentage of profitable trades

## Exploratory Data Analysis

Visualizations created include:

Sentiment distribution (Fear vs Greed)

Average PnL by sentiment

Average trade size comparison

Win rate comparison

Daily PnL trend

These visualizations help understand how trader behavior shifts with market sentiment.

## Performance Analysis

Fear vs Greed markets were compared across:

Average Closed PnL for profitability

Win Rate for trader success

Average Trade Size for volume

Exposure proxy for risk behavior

Leverage (where available) for aggressiveness

## Key Insights Discovered

Traders tend to take larger positions during Greed markets

Risk exposure increases when market sentiment is positive

Profitability does not always improve during Greed, suggesting possible overconfidence behavior

Fear periods show more cautious trade sizing

These patterns indicate behavioral biases in trading decisions.

Final Deliverables

Cleaned and merged datasets

Analytical CSV outputs

Visual charts

ds_report.pdf with summarized findings

Structured project folder ready for submission

## Tools Used

Python

Pandas

NumPy

Matplotlib

ReportLab

## Why This Project Matters

This project demonstrates the ability to:

Perform data cleaning and merging

Analyze financial trading data

Detect behavioral patterns

Engineer meaningful features

Generate strategy-relevant insights

Deliver business-style reporting

## Outcome

This analysis connects market psychology with real trader behavior, helping understand when traders:

Take higher risk

Overtrade

Underperform despite bullish sentiment

These findings are valuable for risk management and trading strategy optimization.

# Average Trade Size by Sentiment Classification

The average trade size (measured using Size USD) varied notably across market sentiment categories.


## Classification-wise average trade size (USD):

Fear: 7,816.11

Greed: 5,736.88

Extreme Fear: 5,349.73

Neutral: 4,782.73

Extreme Greed: 3,112.25

Fear periods were associated with the largest average trade sizes. This indicates that during fearful market conditions, traders tend to deploy more capital per trade, suggesting higher conviction or attempts to capture perceived undervaluation opportunities.

## Visualizations

Daily Average PnL by Sentiment Classification
This visualization shows the fluctuation of average daily Closed PnL across different sentiment states over time. Although no perfectly consistent pattern exists, noticeable spikes in profitability occur during certain sentiment phases, indicating that market mood influences opportunity availability but does not solely determine performance.

Closed PnL Distribution by Sentiment Classification
The box plot of Closed PnL highlights the spread and outliers of profitability for each sentiment state. Large profits and losses are observed across all sentiment categories. This suggests that while sentiment affects behavior, individual trading strategy and execution quality remain the dominant performance drivers.

## Insights and Trading Strategy Recommendations

Capitalize on Fear Periods
Fear periods showed the highest total Closed PnL and the largest average trade sizes. These conditions may create contrarian opportunities where fundamentally strong assets are undervalued due to market anxiety. Traders can consider calculated long positions during these phases, provided confirmation from technical and fundamental analysis is present. Short-selling opportunities may also arise from exaggerated reactions to negative news.

Exercise Caution During Extreme Fear and Extreme Greed
Extreme Fear produced the lowest overall Closed PnL, indicating highly volatile and unpredictable conditions. Traders may benefit from reducing exposure during such phases. Extreme Greed periods, associated with smaller average trade sizes, often signal market overextension. Risk reduction and profit booking may be more appropriate during these times.

Focus on Risk Management and Individual Strategy
The weak direct correlation between the Fear/Greed Index and Closed PnL shows that sentiment alone does not guarantee profitability. Proper risk management through stop-loss placement, position sizing, and disciplined strategy execution remains essential.

Use Sentiment as a Confluence Factor
Market sentiment should be used as a supporting indicator rather than a standalone signal. For example, a technically strong long setup during Fear provides additional confidence, while a short setup during Greed strengthens conviction. Sentiment enhances decision-making when aligned with other analytical tools.

Adapt Trade Size to Sentiment
Since larger average trade sizes were observed during Fear and smaller ones during Extreme Greed, traders may dynamically adjust position sizes. Higher conviction periods can justify larger exposure, while euphoric markets may require reduced risk allocation.
