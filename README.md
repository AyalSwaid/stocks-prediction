# stocks-prediction
Machine Learning project that predicts stocks behavior by analyzing tweets contents about each stock.

# Project Overview
1. Find the emotion behind each tweet using nltk library(emotion is represented by a number between -1(negative) and 1(positive)).
2. For each date in the tweets dataset, find the closest(by date) stock value to it from the stocks dataset, and then assign the tweets' mean compound(Emotion) value to the relevant stocks row in stocks set.
3. Analyze and preprocess the new merged dataset.
4. Build a deep learning model to perform regression using keras package.
5. Fit the model to the merged dataset, such that the target value is stock close value and the features are (open_value, date, mean_emotion)
6. Fit another model that predicts the close value but without the compound(emotion) feature
7. Evaluate both models and find the difference.
8. Conclusion

# Some plots and results

## Number of each stok data in the given dataset
![download](https://user-images.githubusercontent.com/57876635/218337791-83bad1af-2c45-42aa-ab9d-a6cbbf5590e4.png)

## TSLA stocks close values during the given period
![download](https://user-images.githubusercontent.com/57876635/218337839-4ada2176-36f0-47b3-83f0-588844894dd6.png)

## Predicting stocks: once considering tweets emotions and once without considering tweets emotion
![delete drawio](https://user-images.githubusercontent.com/57876635/218338096-f4a951a6-474a-4e52-a2e1-fa0a78a02e14.svg)

## Visualize predicting of stocks on the entire dataset period (30.9.2021 - 30.9.2022)
![download](https://user-images.githubusercontent.com/57876635/218338503-ef42fe3c-e151-40cc-8755-b7e37ef14e35.png)

## Learning rate (without considering tweets)
![history no compound](https://user-images.githubusercontent.com/57876635/218338574-9302c2a6-f9e1-4645-81a5-b1e996427b9e.png)
*Highe Variance and bias + overfitted*

## Learning rate (with considering tweets)
![learning rate drawio (1)](https://user-images.githubusercontent.com/57876635/218339163-fab8fa26-54d2-425b-a818-894915fbf276.svg)

### A closer look on the learning rate
![closer_learning_rate drawio](https://user-images.githubusercontent.com/57876635/218339220-3799a9ba-8864-4de4-8558-68874b5a72c1.svg)

# Conclusion

The model with the compound value has more stable learning rate plot, unlike the model without the compound value its learning rate plot had a high variance and it semmed like it has some randomness with it.
So we conclude that compound value, which is the tweets emotions scale, has a potential to affect the stocks values.

# Future plan
make auto predicting using the following process:
1. get some tweets using api
2. predict according to the tweets
3. show result as plots

# References
* [dataset](https://www.kaggle.com/datasets/equinxx/stock-tweets-for-sentiment-analysis-and-prediction)
