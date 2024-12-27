# My_Achievements
Project Summary: Flight Price Prediction
Objective
The objective of this project is to build a predictive model that estimates flight prices based on various features related to the flights. The project utilizes multiple regression algorithms to compare their performance and identify the best model for predicting flight prices.

Dataset
The dataset used for this project is Data_Train.xlsx, which contains various features related to flights, including:

Total Stops: Number of stops in the flight.
Journey Day: Day of the month when the journey takes place.
Journey Month: Month when the journey takes place.
Departure Hour and Minute: Time of departure.
Arrival Hour and Minute: Time of arrival.
Duration: Total duration of the flight.
Airline: Categorical variable representing the airline.
Source and Destination: Categorical variables representing the source and destination airports.
The target variable for prediction is Price, which represents the cost of the flight.

Methodology
Data Preprocessing:

Loaded the dataset and separated the features (X) from the target variable (y).
Handled categorical variables using one-hot encoding to convert them into a numerical format suitable for machine learning algorithms.
Split the dataset into training (80%) and testing (20%) sets.
Feature Scaling:

Scaled the features using StandardScaler to ensure that all features contribute equally to the model training, especially for algorithms sensitive to feature scales like SVM and KNN.
Model Selection:

Implemented four regression algorithms:
Random Forest Regressor: An ensemble method that builds multiple decision trees and merges them to get a more accurate and stable prediction.
Support Vector Regressor (SVR): A regression algorithm that uses support vector machines to find a hyperplane that best fits the data.
K-Nearest Neighbors (KNN): A non-parametric method that predicts the target variable based on the average of the nearest neighbors.
Decision Tree Regressor: A tree-based model that splits the data into subsets based on feature values.
Model Training and Evaluation:

Each model was trained on the scaled training data, and predictions were made on the test set.
Evaluated model performance using two metrics:
R² Score: Indicates the proportion of variance in the target variable that can be explained by the model. A higher R² score indicates better model performance.
Mean Squared Error (MSE): Measures the average squared difference between predicted and actual values. A lower MSE indicates better model performance.
Hyperparameter Tuning:

Used GridSearchCV to perform hyperparameter tuning for KNN and SVM models to find the optimal parameters that improve model performance.
For KNN, tuned the number of neighbors (n_neighbors).
For SVM, tuned the regularization parameter (C) and the kernel type.
Results
The results of the model evaluations were printed, showing the R² scores and MSE for each algorithm.
The best hyperparameters for KNN and SVM were also printed, indicating the optimal settings for these models.
Conclusion
This project demonstrates the process of building a flight price prediction model using various regression algorithms. The comparison of model performances provides insights into which algorithms are more suitable for this type of prediction task. Future work could involve further feature engineering, exploring additional algorithms, or using more advanced techniques like ensemble methods or deep learning for improved accuracy.
