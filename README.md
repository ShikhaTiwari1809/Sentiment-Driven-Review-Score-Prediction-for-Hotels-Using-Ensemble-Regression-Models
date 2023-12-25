# Sentiment-Driven-Review-Score-Prediction-for-Hotels-Using-Ensemble-Regression-Models
This project predicts hotel review scores using sentiment analysis (VADER). Polarity scores from sentiment analysis serve as features, while reviewer scores are the target. Ensemble regression models, particularly Random Forest, excel due to their ability to handle overfitting and combine multiple trees for accurate predictions.


The project revolves around predicting hotel review scores based on sentiment analysis of customer reviews. Here's a gist of the project description:

Title: "Sentiment-Driven Review Score Prediction for Hotels Using Ensemble Regression Models"

The project aims to quantify anticipated hotel visits by predicting review scores. Initially, it was observed that the unprocessed data lacked correlation with the review score target variable. To enhance analysis, feature engineering was employed, creating new features using VADER sentiment analysis.

VADER Sentiment Analysis: VADER (Valence Aware Dictionary for Sentiment Reasoning) is used for text sentiment analysis, considering both polarity (positive/negative) and intensity (strength) of emotion. Sentiment scores were derived from textual data to gauge opinions and emotions.

Model Pipeline: Pre-processing involved cleaning and tagging text data, followed by sentiment analysis on combined positive and negative reviews to generate polarity scores.

Feature and Target Selection: Polarity scores derived from sentiment analysis were chosen as features, while the reviewer score served as the target variable for prediction.

Regression Models Used:

Decision Tree Regressor
Random Forest Regressor
Adaboost Regressor
Model Selection: Mean squared error (MSE) was employed to compare model performance. Random Forest emerged as the best-performing model due to its lower MSE, attributed to its ability to handle overfitting and combine multiple trees for improved predictive accuracy.

Key Observations:

Random Forest was found to be the most effective model.
The "pos" polarity score was identified as the most crucial feature, potentially due to the skewness towards positive reviews in the dataset.

Model Example

Example 1 -
Review: “Easy access to San Diego main areas. Nice to have good coffee in lobby & brown bag breakfast. Nice staff.”
Vader Sentiment Scores: {'neg': 0.0, 'neu': 0.528, 'pos': 0.472, 'compound': 0.8885} 
Reviewer score for example 1 using random forest regressor: [8.77382355]

Example 2 -
Review: “room was dirty and i was afraid to walk, and bathroom tile floor could have been cleaner. Spots/general soiling on the chairs and the tile was dirty, along with hair and dirt in the corners.”
Vader Sentiment Score: {'neg': 0.206, 'neu': 0.752, 'pos': 0.043, 'compound': -0.7579}
Reviewer score for example 2 using random forest regressor: [5.50503333]
