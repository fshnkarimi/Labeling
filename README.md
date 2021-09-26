In this project, we use a labeling algorithm, different models on some datasets, and a new cross-validation method.
Labeling algorithm: determine trends according to a specific threshold and window size. When the market rises above the threshold from the current lowest point or recedes from the current highest point to the threshold, the two segments are labeled as rising and falling segments. We examine two window sizes, 11 and 44 previous days.
Here we use a low-pass filter for eliminating high frequencies, and we determine our sampling frequency according to the nyquist rate.
Purging: One of the most important problems in time-series data prediction is data leakage between train and test data which causes false accuracy.   
For reducing this data leakage, we remove all observations whose labels overlapped in time with those labels included in the testing set from the training set. This process is called purging.
Models: we have used different models for prediction, such as LSTM, GRU, LR, SVM, and XGBoost.
Datasets: Cryptocurrencies
Buy and sell strategy: This strategy is very simple. When the trend is upward, you buy a stock, hold onto it until the trend changes, and then sell it. 
Metrics: We compare all models with different metrics, such as rate of return, Sharpe ratio, drawdown
