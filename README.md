# Portfolio Risk and Performance of Asset Allocation Weighting Schemes

## Summary
Purpose of this analysis is to study the risk and performance of different weighting schemes when come to asset allocation.  

Two most common weighting schemes in **Modern Portfolio Theory** is the ***Maximum Sharpe Ratio (MSR)*** and the ***Global Minimum Volatility (GMV)*** portfolios.  These 2 portfolios lie on the efficient frontier.  

Togther with two other weighting schemes, namely the ***Equally Weighted Portfolio (EW)*** and the ***Equal Risk Contribution Portfolio (ERC)***, we shall backtest and see how the respective portfolio performs over the same period.

## Asset Allocation Weighting Schemes
1. MSR: Maximum Sharpe Ratio
2. GMV: Global Minimum Volatility
3. EW: Equally Weighted
4. ERC: Equal Risk Contribution (Risk Parity)

## Data
Price data are downloaded from yahoo finance.  Monthly returns are calculated and then used to estimate the asset expected returns and covariance matrix.

## Assets
Three asset classes are selected for this analysis:
- Equity: iShares Core U.S. Aggregate Bond
- Fixed Income: SPDR S&P 500
- Commodity: SPDR Gold Trust

Risk Free Rate: CBOE Interest Rate 10 Year T Note

## Backtesting 
Portfolio is rebalanced at the end of each month using past 36 months of returns.  The portfolio returns for the forward months are calculated and cumulative returns plotted for performance comparison.

## Notebook
https://github.com/edgetrader/asset-allocation-weighting-schemes/blob/master/notebook/asset-allocation-weighting-schemes.ipynb
