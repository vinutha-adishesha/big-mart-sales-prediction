# big-mart-sales-prediction
A predictive model to predict sales for each product at a particular outlet
Big mart sales prediction
The goal is to understand the data, analyse it, find hidden patterns and meaningful features which can contribute to predict the accurate sales
The task is to clean the data, address the missing values we see in Item_Weight and Outlet_Size and apply feature engineering to enrich the data. Visualize and transform the data into required format for the model.
We can understand the data distribution and statistics using describe ()
We use median to impute the Item_weight based on the Item identifier because, weight of the item could be similar in same type of item, median is used as impute strategy because we see skewness in data and median is right metric to address this problem by still maintaining the distribution of the data.
To fill the null values in Outlet_Size, we have grouped them acc to Outlet_type and then used the most appearing size from a category considering the same category outlets will have same size.
Item_Fat_Content has a lot of data inconsistency, once we correct that we can only see two categories in the said feature.
We use histogram and boxplot to check the outliers and skewness in the data. We see that Item_visibility is skewed (right) and hence we use box-cox transformation to normalise the values
We have used value counts to see if there are any categories that are extremely less frequent, which should be merged. We did not find any category that is alarmingly low.
Heatmap to identify the relationship between variables. We have also made use of scatterplot to see the relationship between visibility and sales, which requires looking into as there are high item visibility but extremely low sales. We can look into strategies of marketing etc, there are chances that the values are not correctly collected.
For Featuring engineering, we have created a column from outlet established year to capture the store age and plot showing that the newer stores are doing better with respect to the sales.
We have reduced the cardinality in the Item_type by grouping the types of items to categories like food, non-food and drinks
We have used label encoder to encode the categorical variables into numerical for the model.
Models:
Since the business problem requires us to predict the continuous variable, this is a regression problem. Hence, we are using multiple regression algorithms to make predictions.
We have made use of models like Linear Regression, Random Forest Regressor, Gradient Boosting method, Lasso Regression, Ridge Regression, Catboost algorithm.
We have used gridsearch cv for hyperparameter tunning and choosing the best model
Result: 
Gradient Boosting Model is the champion model which has less RMSE as compared to other models.
Hackathon Rank: Gradient Boosting Model scored 1154.65 RMSE value and the Rank on LeaderBoard is 2000

