# Portfolio Risk and Performance of Asset Allocation Weighting Schemes

## Summary

### Asset Allocation Weighting Schemes
Purpose of this analysis is to study the risk and performance of different weighting schemes when come to asset allocation.  

Two most common weighting schemes in **Modern Portfolio Theory** is the ***Maximum Sharpe Ratio (MSR)*** and the ***Global Minimum Volatility (GMV)*** portfolios.  These 2 portfolios lie on the efficient frontier.  

Togther with two other weighting schemes, namely the ***Equally Weighted Portfolio (EW)*** and the ***Equal Risk Contribution Portfolio (ERC)***, we shall backtest and see how the respective portfolio performs over the same period.

#### Notebook
1. https://github.com/edgetrader/asset-allocation-weighting-schemes/blob/master/notebook/asset-allocation-weighting-schemes.ipynb

---
### Impact of Parameter Estimations on Porfolio Risk and Performance
Most asset allocation weighting schemes rely on security expected returns and covariance estimation.  Slight changes to these estimations may have significant impact to the weights in asset allocation and hence the portfolio performance.  Portfolio managers and analysts estimate these parameters differently based on data availability,  investment horizon and rebalancing frequency.

Expected returns and covariance estimation considerations:
1. Return horizon - eg: Yearly, Monthly, Weekly, Daily?
2. Return period - eg: 10, 5, 3, 2, 1 years?
3. Covariance on Sample Returns - Depending on return horizon?
4. Covariance on Sample Returns assuming constant correlation
5. Covariance with Statistical Shrinkage

Things to notes:
1. Selecting return periods depend on price history.  Depending on investment horizon, historical data that are too old may be a good reflection of current market conditions.  On the other hand, too short a history may not have enough data points to produce a good estimation of the parameters.
2. Select return horizon depends a lot on rebalance strategy and investment horizon.  Too short a horizon will may generate data points that are too noisy.  At the same time, it will mean more frequent rebalancing and hence higher transaction cost which is not taken into consideration in this analysis.

#### Notebook
1. https://github.com/edgetrader/asset-allocation-weighting-schemes/blob/master/notebook/asset-allocation-parameter-estimation.ipynb

---
### Black-Litterman Asset Allocation Model
The Black-Litterman asset allocation model provides a methodical way of combining investors' subjective views of the future performance of a risky investment asset with the views implied by the market equilibrium.

#### Notebook
3. https://github.com/edgetrader/asset-allocation-weighting-schemes/blob/master/notebook/asset-allocation-black-litterman-basic.ipynb

---
## Data
Price data are downloaded from yahoo finance.  Monthly returns are calculated and then used to estimate the asset expected returns and covariance matrix.

## Backtesting 
Portfolio is rebalanced at the end of each month using past 36 months of returns.  The portfolio returns for the forward months are calculated and cumulative returns plotted for performance comparison.


