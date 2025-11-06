# Market-Sentiment-Analysis

Uncovering Winning Strategies: Trader Behavior vs. Market Sentiment
​This repository contains a data-driven analysis of over 211,000 crypto trades from Hyperliquid, cross-referenced with the daily Bitcoin Fear & Greed Index. The goal was to uncover hidden patterns in trader behavior and identify a provably "smarter trading strategy."
​The analysis uncovered a clear and powerful insight: The most successful traders win by selling into "Extreme Greed," while the least successful traders lose by buying directly into it.
​The "Alpha": The Single Most Valuable Insight
​After analyzing all trades, the key differentiator between profit and loss became clear. It's not just about "buying the fear," but more importantly, about how traders behave during "greed."
​The Winning Strategy: Top-performing traders are disciplined. They buy during "Fear" but achieve their outsized success by aggressively selling when the market sentiment is "Extreme Greed," netting an average profit of $572 per trade.
​The Losing Mistake: Bottom-performing traders are emotional. They fall into the "FOMO" trap and buy during "Greed" and "Extreme Greed," leading to catastrophic losses (averaging -$285 and -$106 per trade, respectively).
​In short, the most successful traders are the ones selling their assets to the least successful traders at the peak of market greed.
​Key Evidence: The Data Behind the Insight
​The patterns were not subtle. The data clearly shows what is happening in the market and who is capitalizing on it.
​1. The Market Pattern: "Buy the Fear, Sell the Greed" is Real
​When analyzing all 211,218 trades, a clear pattern emerged:
​Buying Fear: Buying during "Fear" is profitable, averaging $63.93 in profit.
​Selling Greed: Selling during "Greed" is even more profitable (avg. $59.69), but selling during "Extreme Greed" is the most profitable move on average, at $114.58 per trade.
​The Greed Trap: The single worst action is buying during "Extreme Greed," which barely breaks even with an average PnL of only $10.50.
​This chart clearly visualizes the average profit (or loss) for buying and selling during each sentiment period:
​2. The Behavioral Pattern: Top vs. Bottom Traders
​This is the most critical finding. I segmented traders into the Top 10% (by total profit) and Bottom 10% to compare their specific strategies. The results are stark:
​Top 10% Traders: How They Win
​(Average PnL per trade)
Classification Side mean count
Extreme Greed BUY $1.01 952
Extreme Greed SELL $572.38 1,859
Greed BUY $91.73 4,713
Greed SELL $109.97 4,924
Fear BUY $102.65 11,645
Fear SELL $86.47 11,556
Observation: Top traders almost stop buying during "Extreme Greed" (avg. $1.01 profit). Instead, they sell heavily and are rewarded with an incredible $572 per trade.
​Bottom 10% Traders: How They Lose
​(Average PnL per trade)
Classification Side mean count
Extreme Greed BUY -$106.63 168
Extreme Greed SELL $217.86 211
Greed BUY **-$285.11** 1,618
Greed SELL $11.14 740
Fear BUY $124.25 1,905
Fear SELL -$0.31 3,435
Observation: Bottom traders do the exact opposite. They buy into "Greed" and "Extreme Greed," taking massive losses ( -$285 and -$106 per trade). They are the ones providing the liquidity for the top traders to exit their positions.
​My Actionable "Smarter Trading Strategy"
​Based on this data, a simple, data-driven strategy can be formulated:
​The Golden Rule: Sell Greed. The single most profitable, high-conviction action is to SELL (take profit) when the market sentiment is "Greed" or "Extreme Greed."
​The #1 Mistake: Don't Buy Greed. The fastest way to lose money is to BUY (FOMO) when the market is at its peak. This analysis shows you are likely buying from a top-performing trader.
​The Entry Signal: Buy Fear. The market average holds true. A solid entry signal is to BUY during periods of "Fear."
​Other Key Visuals
​Average PnL by Market Sentiment
This chart shows that, overall, the highest average profits per trade are captured during "Extreme Greed" (driven by the "Sell" orders we identified).
​Average Trade Size by Market Sentiment
This chart shows that traders are most active and commit the largest amount of capital, on average, during periods of "Fear."
​Methodology
​Data Loading: Loaded historical_data.csv (211,224 trades) and fear_greed_index.csv (2,644 days).
​Data Preparation: Converted Timestamp IST (trades) and date (sentiment) from strings to datetime objects. Created a common trade_date key for merging.
​Merging: Joined the two datasets on trade_date, linking every trade to the sentiment of that day.
​Aggregate Analysis: Grouped all trades by classification (sentiment) and Side (BUY/SELL) to find the baseline market profitability.
​Behavioral Segmentation: Calculated the total Closed PnL for every unique Account. Isolated the Top 10% and Bottom 10% of traders by this metric.
​Comparative Analysis: Re-ran the analysis from Step 4 on the df_top_traders and df_bottom_traders DataFrames to identify the specific behavioral differences that lead to profit or loss.
