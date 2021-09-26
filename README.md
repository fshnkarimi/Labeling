In this project, we use a labeling algorithm, different models on some datasets, and a new cross-validation method. The labeling algorithm determine trends according to a specific threshold and window size. When the market rises above the threshold from the current lowest point or recedes from the current highest point to the threshold, the two segments are labeled as rising and falling segments. We examine two window sizes, 11 and 44 previous days. Here we use a low-pass filter to eliminating high frequencies, and we determine our sampling frequency according to the nyquist rate.
One of the most important problems in time-series data prediction is data leakage between train and test data which causes false accuracy. For reducing this data leakage, we remove all observations whose labels overlapped in time with those labels included in the testing set from the training set. This process is called purging.
We have used different models for prediction, such as LSTM, GRU, LR, SVM, and XGBoost, and we test this models on Cryptocurrencies.
We use Buy and sell strategy in which when the trend is upward, you buy a stock, hold onto it until the trend changes, and then sell it. We compare all models with different metrics, such as rate of return, Sharpe ratio, and drawdown.
