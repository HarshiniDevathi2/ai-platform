This code uses two time series datasets in R namely 'austres'(Number of residents in Australia over each quarter) 
and 'BJsales' (sales data). It leaves out the last 'testno' number of points to test the accuracy of each forecasting 
method and to calculate RMSE. Four different methods are currently used:
1. auto.arima 
2. Gaussian process regression with squared exponential kernel function
3. Gaussian process regression with Vanilladot kernel function
4. Prophet library

The user has the option to select the dataset. BY specifying dataset_no=1, 'austres' dataset is used which exists in the base R library 'datasets'.
By specifying dataset_no=2, 'BJsales' dataset is used. This also exists in the base R library 'datasets'.
The number of test instances can also be changed. Currently, the default value for testno is 20. 

The command line command for running this code is 

mlflow run --no-conda <url of the github repository> -P dataset_no={some_value} -P testno={some_value}

To use the default parameters, the command is 

mlflow run --no-conda <url of the github repository>

Option to run from local directory after downloading:

cd <the directory in which files are downloaded to>

mlflow run --no-conda . -P dataset_no={some_value} -P testno={some_value}

To use the default parameters, the command is 

mlflow run --no-conda .

Run 'mlflow ui' to launch the MLflow tracking UI

The UI will be visible at http://localhost:5000 by default.

Background on the datasets:

'austres' is a time series dataset available in base package 'datasets' in R. It records the number of residents in Australia every three months. 
'BJsales' is a time series dataset available in base package 'datasets' in R. It records sales information for 150 consequent time steps. It has a frequeny of 1. 
Much more information is not avilable on this dataset in the public domain.  


