# Solar-Power-Prediction
INTRODUCTION
Regression analysis consists of a set of machine learning methods that allow us to predict a continuous outcome variable (y) based on the value of one or multiple predictor variables (x).
Briefly, the goal of the regression model is to build a mathematical equation that defines y as a function of the x variables. Next, this equation can be used to predict the outcome (y) on the basis of new values of the predictor variables (x).

OBJECTIVE
The objective for the project was to predict solar power generation for the first 28 days of October 2019,  i.e. 1st October 2019 to 28th October 2019, using the weather data for the same period.

HYPOTHESIS
A strong correlation between the various weather parameters (like rainfall type, humidity, temperature, atmospheric pressure) and solar power generation.
Wind gust, UV index, ozone and precipitation intensity have some relation with other weather parameters and thus that relation was exploited in imputing missing values in data preprocessing phase using linear regression.  

MATERIAL AND METHODS
Data Preprocessing- Since the data provided for the power forecast was very noisy data preprocessing phase was very necessary. The involved processes were - 

Missing value imputation - Using other weather data some weather parameters, in which there were outliner and missing value, were imputed using linear regression.
Feature Extraction- Dimensionality was reduced by eliminating the features which were not present in most of the training set phase.
Mean- Features like pressure were more missing on an irregular basis and can be replaced by the mean of pressure.

 Data Analysis (plotting graphs)- After the processed weather data, the analysis was done using power-time graph, which showed the peak of power was in summer months and when plotted for a short period describes that solar power was produced in the day time from 6:00 AM to 6:00 PM. Data was further manipulated according to it by reducing the number of rows in the dataset.

Training of Model - One hot encoding the categorical variables and using standard scaling, the model was trained using methods like linear regression, SVR, CART, KNN. Using k-fold cross-validation method, several models were tested using average accuracy and variance for methods. 
This showed that SVR gives the highest accuracy and lowest standard deviation among all models when tested on 10% of the training data itself (using k-fold cross-validation)
Further, to tune parameters for the SVR model various values were tested for parameters like ‘max_iter’, ‘c’ (penalty parameter) and ‘tol’. 
Using kernel PCA dimensionality reduction was also tried but does not result in an increment in the accuracy. The condition of the atmosphere (Humidity and vapour pressure) and the temperatures (SurfaceTemperature and Air-Temperature) affect the power generation most from the available dataset.
Results were obtained as Y_pred in the python notebook which was the used to create a CSV file in excel. 

CONCLUSION
This study proposes a two-step approach to solar power generation prediction to fully exploit the information contained in the weather data. Specifically, the predicted values for auxiliary variables contribute greatly to enhancing prediction performance.
