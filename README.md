# DengAI
This is a project given from an online data science competition to predict the number of dengue cases each week (in each location) based on environmental variables describing changes in temperature, precipitation, vegetation, and more.

## Predicting Dengue

Our project is structured as a single jupyter-notebook `report-predicting-dengue` which contains all analysis. 

### Feature Engineering and Selection

We attempted to employ the use of Recursive Feature Selection by recursive feature elimination (RFE), which recursively considers successively smaller sets of features and returns a rank based on linear correlation. We modeled using these selected features, but they produced suboptimal results when compared with features selected from domain research. For this reason, we decided not to include the model attempts that employ the use of RFE.

We created new features, rolling averages of features selected by domain knowledge. As these features were temperature and weather data, we believe that employing a rolling mean will better capture the seasonal patters in climate conditions. We chose a window of 1 year (52 weeks) as a repeatable unit of analysis.

### Modeling

For each of our 4 selected algorithms, we performed a gridsearch to find the best parameters for performance based on mean absolute error score. We also have compared each new model to the baseline to assess performance. Models were tuned through succesive runs with gridsearch to narrow the windows of hyper-parameter settings.

Our 4 algorithms:
1) XGBOOST
2) Random Forest
3) Gradient Boost
4) Support Vector Machine

### Validation and Visualization

We are validating and visualizing our model by performing 4 analyses:

1) Showing feature importance
2) Plotting time series of predicted vs. actual cases
3) Plotting scatter plot of predicted vs. actual cases
4) Plotting the prediction residuals

We will use these to compare assess the performance, compare the predictions, and compare the accuracy across all models.

### Best Mean Absolute Error Score

Our lowest MAE is 23.1923