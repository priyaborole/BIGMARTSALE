Big-Mart-Sales-Hackathon This Hackathon is sponsored by Analytics Vidhya and we are supposed to build a predictive model and find out the sales of each product at a particular store. We have train (8523) and test (5681) data set, train data set has both input and output variable(s). We need to predict the sales for test data set.This project predicts the sales of items for BigMart using machine learning. The goal is to develop a robust model that can predict Item_Outlet_Sales based on various features from the dataset. Data Loading & Exploration: The script reads training and test data from CSV files (train.csv and test.csv), checks for missing values, and provides a brief statistical summary along with visualizations.

Data Preprocessing: A preprocessing pipeline is built using a ColumnTransformer and Pipeline from scikit-learn. The pipeline includes: 
Numerical Features: Imputation using the median and scaling with StandardScaler. Categorical Features: Imputation using the most frequent value and one-hot encoding using OneHotEncoder.

Modeling: The project employs a stacking ensemble approach: Two base regressors: RandomForestRegressor and GradientBoostingRegressor. A LinearRegression model is used as the meta-estimator. Additionally, hyperparameter tuning is performed using GridSearchCV to improve model performance.

Evaluation: The best model is selected based on validation RMSE, and predictions are made on the test dataset. Negative predictions are clipped to zero since sales cannot be negative.

Submission File Creation: A submission file is generated with three required columns: Item_Identifier, Outlet_Identifier, and Item_Outlet_Sales.

Our machine learning model for BigMart sales prediction successfully identified key patterns in the dataset and achieved a strong performance. The final stacking ensemble model, consisting of RandomForestRegressor and GradientBoostingRegressor as base learners and LinearRegression as a meta-learner, provided the best results with an RMSE on the validation set.Best Model: GradientBoostingRegressor with RMSE = 1039.18977
