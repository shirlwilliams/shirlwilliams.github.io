---
layout: post
title:      "Feature Importance"
date:       2020-05-14 19:13:51 +0000
permalink:  feature_importance
---


While working with XGBoost in my customer churn model I found myself exploring feature importance. Something didn't add up and I was having trouble explaining why. That's when I stumbled across this article: [Interpretable Machine Learning with XGBoost](https://towardsdatascience.com/interpretable-machine-learning-with-xgboost-9ec80d148d27)

In the article I discovered not one but three options for measuring features in XGBoost: weight, cover, and gain.

* Weight provides the number of times a feature is used to split the data across all trees.
* Cover provides the number of times a feature is used to split the data across all trees weighted by the number of training data points that go through those splits.
* Gain provides the average training loss reduction gained when using a feature for splitting.

Evaluating the consistency and accuracy when applying these options help us to choose the best reresentation for feature importance.
