# Housing_SalePrice_Prediction - Dataset from Kaggle competition

This project aims to predict the selling price of a houses based on various factors like LivingArea, YearBuilt, OverallQuality, OverallCondition etc. (predictor variables).

First a through Exploratory Data Analysis was done which included univariate and multi-variate analysis, data cleaning, plotting graphs etc.  

Then we used Stacking Base Models appoach for training. Basically, we train our base models, Kernel Ridge Regression, Lasso, Elastic Net and Gradient Boost and stack them together by averaging them. This gives us our stacked regressor.

Next, we also used Stacking Base Models with meta-learner. Here, suppose we have 4 base models and 1 meta-model, the training process will be done as follows:
- First, training set is divided into two parts, train and hold_out.
- Training will be done on train set and the hold_out set will be used for prediction.
- This will be done for all the base models and the iterations will be defined by 'k' as defined in k-fold CV.
- The predictions by each base model then serves as new feature on which our meta-model is trained.
- As for during testing phase, the predictions from all the models on the test data are averaged which results in formation of   meta-features on which final predictions are done by our meta-model.

To learn more about stacking, please refer:
http://blog.kaggle.com/2017/06/15/stacking-made-easy-an-introduction-to-stacknet-by-competitions-grandmaster-marios-michailidis-kazanova/

  
Finally, we stack together the results from Stacked Regressor with meta-model, xg_boost and lg_boost in order to get the best result.

References:  
https://www.kaggle.com/serigne/stacked-regressions-top-4-on-leaderboard 

https://www.kaggle.com/pmarcelino/comprehensive-data-exploration-with-python
