# House Price Prediction Model

## Project Overview

This project focuses on predicting house prices using the **California Housing dataset**. The primary objective is to build a robust regression model to estimate house prices based on various factors such as median income, house age, average number of rooms, and other relevant features.

The model leverages **XGBoost**, a powerful gradient boosting framework, to achieve high accuracy in predictions.

## Dataset

The **California Housing dataset** consists of 20,640 rows and 9 columns. Each row represents a region in California, and the columns provide data on:

- **MedInc**: Median income in the region
- **HouseAge**: Median house age in the region
- **AveRooms**: Average number of rooms per household
- **AveBedrms**: Average number of bedrooms per household
- **Population**: Population in the region
- **AveOccup**: Average number of household members
- **Latitude**: Latitude of the region
- **Longitude**: Longitude of the region
- **Price**: Median house value (target variable)

## Data Preprocessing

1. **Loading and inspecting the dataset**: The dataset was loaded using the `sklearn.datasets.fetch_california_housing()` function and converted into a pandas DataFrame for further analysis.
2. **Handling missing values**: There were no missing values in this dataset.
3. **Splitting the data**: The data was split into features (X) and the target variable (Y). We then used an 80/20 train-test split using `train_test_split` from `sklearn.model_selection`.

## Model

We utilized the **XGBoost Regressor** to train the model. The model is an ensemble learning method that combines weak learners to create a strong prediction model. Key parameters and features of the XGBoost model include:

- Handling missing data
- Ability to work well with structured/tabular data
- High-performance accuracy for regression tasks

### Model Training

- The model was trained using the training set, which consists of 80% of the data.
- **R-squared error** and **mean squared error** were used to evaluate the model performance on both the training and test datasets.

## Evaluation

1. **Training Set Performance**:
   - **R-squared error**: 0.943
   - **Mean squared error**: 0.074

2. **Test Set Performance**:
   - **R-squared error**: 0.833
   - **Mean squared error**: 0.223

The results show that the model performs well, with an R-squared value close to 1, indicating a good fit for both the training and testing datasets.

## Visualization

To further understand the model performance, we visualized the predictions using scatter plots:

- **Training Set**: A scatter plot comparing actual vs. predicted house prices.
- **Test Set**: A similar plot for the test dataset.

## Conclusion

This project demonstrates the effectiveness of the XGBoost regression algorithm for house price prediction. The model achieved a good fit with high R-squared scores and low mean squared errors, making it suitable for predicting house prices based on the given features.

## Usage

To use the model, follow these steps:

1. Clone the repository.
2. Install the necessary dependencies listed in the `requirements.txt`.
3. Run the `house_price_prediction.ipynb` notebook to load the dataset, preprocess the data, train the model, and evaluate its performance.
