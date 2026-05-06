**Introduction**

*Write your answers in the Intro section of your notebook.*

To get started, please write 5 examples of the application of ML methods in life. What is the benefit of using machine learning methods in each of your examples?
Use the classification of tasks in the introduction to decide which class you can assign to the tasks from the table above and to the 5 examples you provided.
Think about what the difference is between multiclass and multilabel.
Is an example case with house prices from the theory a classification of a regression problem? Is it possible to reduce the regression problem to classification?

*Introduction to Data Analysis*

- Import the libraries pandas, numpy, sklearn, lightgbm, scipy, statsmodels, matplotlib, seaborn. Use pip install if necessary.
- Load data from kaggle using pandas. You only need the table data, which is in train.json.
- What is the size (the number of rows and columns) of your data?
- Print the list of columns. Which column is a target?
- Make a quick analysis of the data: use the methods info(), describe(), corr(). Explain the results of the outputs. Are there any empty columns?
- We'll work with only 3 features: 'bathrooms', 'bedrooms', 'interest_level' and with the target column 'price'. Create a dataframe with only these columns.

*Statistical Data Analysis*

- To get started with statistical data analysis, we recommend that you refresh your basic knowledge of statistics, such as Mean / Median / Mode / Variance / Standard Deviation. Also you are welcome to be free with distributions (Discrete uniform Distribution, Bernoulli Distribution, Binomial Distribution, Poisson Distribution, Normal Distribution, Exponential Distribution). Please make sure that you know the definitions of outliers, percentiles, confidential intervals. The article will be presented later.
- Have a quick look at this article. Please pay attention to such aspects as distributions and histograms, boxplots, outliers, kernel density function.
- Target analysis
- Plot a histogram to understand the distribution of the target. Is it all clear?
- The next step is boxplot(). What can you say about the target? Are there any outliers?
- Drop the rows that are outside the 1 and 99 percentiles from the target column.
- Plot another histogram for price. Explain the result.

*Characteristics Analysis*

- What is the type of column 'interest_level'?
- Print the values in this column. How many entries does each value contain?
- Encode these values. For example, you can replace each value with 0, 1, or 2.
- Plot histograms for the features 'bathrooms', 'bedrooms'. Are there any outliers?

*Complex analysis*

- Plot a correlation matrix to understand the correlation between features and target. Plot a heat map for the correlation matrix. Is there a correlation?
- Plot a scatterplot to visualize the correlation between the features and the target. You should return 3 plots where the X-axis is the target and the Y-axis is a feature.

*Creating Features*

- This step is very broad. You can create as many features as you want. For example, you can add 3 new features that are squared: 'bathrooms_squared', 'bedrooms_squared', ''interest_level_squared'. Plot a correlation matrix with the new features. Are the new features more correlated with the target than the basic features?
- To train the model here, we will not use your new features. Remember this example and use it in Lecture 2. To train the model, we will only consider the features 'bathrooms' and 'bedrooms'.
- Read this Sklearn info about PolynomialFeatures.
- To use PolynomialFeatures, we first need to split the data into training and test samples. We have already done this for you, please read the training and test data.
- Initialize PolynomialFeatures() with a degree of 10.
- Apply PolynomialFeatures() to fit and transform your training and test data.
- Now you need to train 3 models: linear regression, decision tree and naive model. We will use them as black boxes without deep understanding.

*Results table*

- Create two empty Pandas DataFrames with columns 'model', 'train', 'test'. Let's call the first one result_MAE and the second one result_RMSE. We will fill these tables with the results of the models.

*Linear Regression*

- Initialize linear regression from sklearn with no parameters.
- Fit your model and make predictions on training and test features. Save it as new columns in data.
- Compute MAE (Mean Absolute Error) on training and test targets.
- Calculate RMSE (Root Mean Square Error) on training and test objectives.
- Insert your metrics into tables result_MAE and result_RMSE with model name 'linear_regression'.

*Decision Tree*

- Initialize decision tree regressor from sklearn with fixed random_state=21.
- Fit it to train features and train target and make prediction on train and test features. Save it as a new column in data.
- Compute MAE (Mean Absolute Error) on train and test targets.
- Compute RMSE (Root Mean Square Error) on train and test targets.
- Insert your metrics into tables result_MAE and result_RMSE with model name 'decision_tree'.

*Naive Models*

- Calculate the mean and median of 'price' on the training and test data and create a column with these values.
- Calculate the MAE on the training and test targets between your target and the calculated mean and median.
- Calculate the RMSE on the training and test targets between your target and the calculated mean and median.
- Insert your metrics into tables result_MAE and result_RMSE with model names 'naive_mean' and 'naive_median'.

*Compare the results*
- Print your final result_MAE and result_RMSE tables.
- Which is the best model?
