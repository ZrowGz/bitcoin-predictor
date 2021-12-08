YOLO Bot - An algorithmic trading bot

## Project Proposal

Analyze Bitcoin data from Glassnode API to create Buy or Sell signal.
Utilize machine learning models to find which one is the most accurate.
    * SVM: https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html
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
