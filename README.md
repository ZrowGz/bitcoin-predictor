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

## Data Source
 
 For our data source we used data from [Glassnode](https://studio.glassnode.com/metrics?a=BTC&m=addresses.ActiveCount). Running the code in the GLASSNODEPULL.ipynb file will export the data into a csv file.
 The 16 metrics we used for our models were:
 
|   |  | |  |
| ------------- | ------------- | ------------ | ------------- |
| price  | a-sopr  | puell_multiple  | exchange_netflow  |
| difficulty_compression_band	|mvrv_z_score | nonzero_balance_addresses |	%_utxo_in_profit |
| nvt |	nupl | stablecoin_supply |	rhodl |
|cvdd	| rpv |	balanced_price |	investor_capitalization |

Information about these metrics can be found at the following site: [Glassnode Academy](https://academy.glassnode.com/)

## Installation

To clone the repository use the following line of code:

    git clone https://github.com/ZrowGz/trading-bot.git
To use the code the required libraries will need to be installed (unless using Google Colab). This can be installed by running the following line of code:

    pip install -r ./requirements.txt

**An API Key from Glassnode is required for pulling data. [How to get an API Key](https://docs.glassnode.com/basic-api/api-key)** <br>
**If wanting to run the code on MacBook an M1 chip, [Google Colab](https://research.google.com/colaboratory/) will need to be used**
