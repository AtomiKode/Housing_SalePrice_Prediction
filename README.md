# Housing_SalePrice_Prediction
Predicting selling price of a houses based on various factors like LivingArea, YearBuilt, OverallQuality, OverallCondition etc. (predictor variables).

In this project we have used Stacking Base Models appoach. Basically, we train our base models, Kernel Ridge Regression, Lasso, Elastic Net and Gradient Boost and stacked them together by averaging them.

Next, we also use Stacking Base Models with meta-learner. That is if we train 4 base models and stack them by averaging, the fifth model will be trained inddividually.  
