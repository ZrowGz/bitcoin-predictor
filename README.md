YOLO Bot - An algorithmic trading bot

## Project Proposal

* Python based.  
* Use Glassnode API.  
  * indicators tbd.  
* Select charts.  
  * aSOPR: https://studio.glassnode.com/metrics?a=BTC&category=Ratios&m=indicators.SoprAdjusted&s=1580401206&u=1638230400&zoom=
  * Funding Rates: might not have date
  * NUPL: https://studio.glassnode.com/metrics?a=BTC&category=Profit%2FLoss&ema=90&m=indicators.NetUnrealizedProfitLoss&mAvg=0&mMedian=0&s=1232323200&u=1638230400&zoom=
  * Exchange Netflows: https://studio.glassnode.com/metrics?a=BTC&category=Entities&m=transactions.TransfersVolumeExchangesNet&s=1580401206&u=1638230400&zoom=
* Plug glassnode chart api data into machine learning to create a Buy, Hodl, or Sell signal (1, 0, -1).  
  * machine learning models to try include: 
    * SVM: https://scikit-learn.org/stable/modules/svm.html
    * Logistic Regression: https://scikit-learn.org/stable/modules/linear_model.html#logistic-regression
    * Neural Networks: https://scikit-learn.org/stable/modules/neural_networks_supervised.html
* Backtest the algorithm through the previous 4 years, reduce if data load is too great.  
* Analyze the profitability of the trading algorithm through visualizations.  
  
Optional: Add an api that allows taking action through a paper trading platform (alpaca).  


Breakadown of code components
