Obective of the Problem:
Predicting the power that is generated in(KM/h) based on the features given in the dataset

Collecting of Data:
I have downloaded the data from the hacker earth competation "Predict the power (KM/h) produced from the windmills"
In this dataset there are 3 files which is of train.csv, test.csv and sample_submission.csv .
By using train and test data i need to predict the outcome of windmill_generated_power(kW/h) for the test data there should be 12086 rows and 3 columns

Preprocessing the data:
In this preprocessing there are so many null values so here in this dataset i have removed all the null values  by replacing with their corresponding column means.
In the data there is a column called cloud_level in that there are 3 items which is Low, Medium and Extremly Low, so i replaced all the strings with integers as 0,1,2.
I droped the turbine_status column because that is not used and it is contained with string values and it will through the error while do the model training.

Model Building:
By seeing the data we can say this is an regression problem. Regression problem means y is dependent on x.
so i spilt the data into X and y variables.
Here X is know as independent and i considered all the columns except tracking_id,datetime and windmill_generated_power(kW/h).
Where y is considered as windmill_generated_power(kW/h).
By using all the values i have created the model which is of Linear Regression, Decision Tree Regressor, Random Forest Regressor, XGboost Regressor, KNeighbors Regressor and few.

Model Evaluating :
Out of all the models i got good accuracy in Random Forest Regressor and i used that model for my model evaluation.
I got 99.13% accuracy while testing.

Prediction:
I predicted the given test.csv data.
After Predicting i have created a new csv file using tracking_id, datetime and windmill_generated_power(kW/h) as the features which is in 'submission_output1.csv' with          12086 rows and 3 columns.


