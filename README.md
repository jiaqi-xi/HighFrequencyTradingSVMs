# High Frequency Pairs Trading Strategy using KNNs
This is an Algorithmic Trading Project that implements a high frequency trading strategy that utilizes KNNs to capture statistical arbitrage in the pricing of Class A and Class C Under Armour stocks. The overall idea is Pairs Trading, a nondirectional, relative-value investment strategy that seeks to identify two companies with similar trading characteristics. We will demonstrate a trading algorithm that earns great profit with a sharpe ratio of 6.8 over 2 years.


## Instructions

Code is mainly located in `./noteboooks`.

1. Run `Data_Exploration.ipynb`.
   - Download Data from Alpha Vantage and store in `./data/ua.csv` and `./data/uaa.csv`.
   - Turn time column into datetime formula.
   - Align the two stock data by time and store in  `./data/df_ua.csv` and `./data/df_uaa.csv`.
2. Run `Feature_Creation.ipynb`.
   - Generate four technical indicators and store in  `./data/df_ua_processed.csv` and `./data/df_uaa_processed.csv`.
   - Generate train_test_folds and store in  `./data/info.npy`. **Note that this file is too large to be uploaded. Please generate it yourself.**
   - Generate plots in `./plots/fold_plots` and `./plots/residual_plots` if set `plot=True`.
3. Run Model Tuning notebooks, e.g. `SVM Model Tuning.ipynb`.
   - Do gridsearch and store results in `./data/gridsearch_results_***.pkl`.
4. Run `Backtesting_backup_models.ipynb`.
   - Manually input the best parameters and do backtesting.
   - Generate plots in `./plots/backtesting`.
5. Run `Sensitivity_Analysis.ipynb`.
   - Experiment on how changes of parameters influence our backtest results.

