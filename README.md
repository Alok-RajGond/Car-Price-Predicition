# OIBSIP_TASK_NO.-3

# Car Price Prediction

This project aims to predict the prices of cars based on various features such as fuel type, car body, engine, transmission, etc.

## Dataset

The dataset used for this project is stored in a CSV file named "CarPrice.csv". It contains information about different cars and their corresponding prices. The dataset has the following columns:

- car_ID: Unique identifier for each car
- CarName: Name of the car
- fueltype: Fuel type of the car (gas or diesel)
- carbody: Body type of the car (convertible, hardtop, hatchback, sedan, wagon)
- drivewheel: Type of drive wheel (4wd, fwd, rwd)
- enginelocation: Location of the car's engine (front or rear)
- wheelbase: Wheelbase of the car
- enginetype: Type of engine
- enginesize: Size of the car's engine
- curbweight: Weight of the car without occupants or baggage
- fuelsystem: Type of fuel system
- boreratio: Bore ratio of the car's engine
- stroke: Stroke length of the car's engine
- horsepower: Horsepower of the car
- peakrpm: Peak revolutions per minute
- citympg: Miles per gallon in the city
- highwaympg: Miles per gallon on the highway
- price: Price of the car (target variable)

## Data Preprocessing and Exploration

The project begins with loading the dataset using pandas library. The data is then explored by checking the shape of the dataset, column names, and the presence of missing values. The data types of the columns are also checked and converted to the appropriate types if needed.

Data preprocessing steps include handling missing values and removing unnecessary columns. Exploratory data analysis is performed using various visualization techniques such as histograms, count plots, and scatter plots to understand the distribution and relationships between variables.

## Feature Engineering and Encoding

To prepare the data for model training, feature engineering techniques are applied. The 'cylindernumber' column is converted to numeric values, and dummy variables are created for categorical columns like 'fueltype', 'carbody', 'drivewheel', and 'enginelocation'. These encoded features are then concatenated with the original dataset.

## Model Training and Evaluation

The dataset is split into training and testing sets. A Linear Regression model is trained on the training set and evaluated on the testing set using the R-squared score. Cross-validation is performed to assess the model's performance and to mitigate overfitting.

Additionally, a grid search is conducted to find the best hyperparameters for different models, including Linear Regression, Lasso, and Decision Tree Regressor. The best model is selected based on the highest cross-validated score.

## Prediction

The trained model is then used to make price predictions for new car instances. A helper function `predict_price` is created, which takes the input features such as symboling, fuel type, car body, drivewheel, enginelocation, car length, car width, car height, cylinder number, stroke, and horsepower. The function returns the predicted price for the car.

## Conclusion

This car price prediction project demonstrates the process of building a regression model to predict car prices based on various features. It highlights the importance of data preprocessing, feature engineering, model selection, and evaluation. The trained model can be used to estimate the prices of cars based on their characteristics.

Please make sure to download the "CarPrice.csv" dataset and update the file path in the code before running the project.

Note: The code provided is a summary of the steps involved in the project. It may require additional modifications

 and fine-tuning based on your specific requirements and dataset.
