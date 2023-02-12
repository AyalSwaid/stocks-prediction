# stocks-prediction
Machine Learning project that predicts stocks behavior by analyzing tweets contents about each stock.

# Project Overview
1. Find the emotion(compound value) behind each tweet using nltk library.
2. For each date in the stocks dataset, find the closest(by date) tweets to it, and then assign the tweets' mean compound value to the relevant stocks row in stocks set.
3. Analyze and preprocess the new merged dataset.
4. Build a deep learning model to perform regression using keras package.
5. Fit the model to the merged dataset, such that the target value is stock close value and the features are (open_value, date, compound(emotion))
6. Fit another model that predicts the close value but without the compound feature
7. Evaluate both models and find the difference.
8. Conclusion

# Future plan
make auto predicting using the following process:
1. get some tweets using api
2. predict according to the tweets
3. show result as plots

# References
* [dataset](https://www.kaggle.com/datasets/equinxx/stock-tweets-for-sentiment-analysis-and-prediction)
