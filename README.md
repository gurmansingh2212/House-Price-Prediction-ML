# House Price Prediction Using Machine Learning

A beginner-friendly machine learning project that predicts **California housing prices** using **Linear Regression**. The project covers exploratory data analysis, feature scaling, model training, evaluation, and model serialization.

**Author:** Gurman Singh

## Project Overview

This notebook uses the California Housing dataset provided by Scikit-learn. It explores housing-related features and trains a regression model to estimate median house values.

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Pickle
- Jupyter Notebook / Google Colab

## Dataset

The dataset is loaded directly using `sklearn.datasets.fetch_california_housing()`.

Features: `MedInc`, `HouseAge`, `AveRooms`, `AveBedrms`, `Population`, `AveOccup`, `Latitude`, and `Longitude`.

Target: median house value (`Price` in the notebook), expressed in units of $100,000.

## Workflow

1. Load the California Housing dataset and create a Pandas DataFrame.
2. Inspect the data, missing values, descriptive statistics, and correlations.
3. Visualize feature relationships and distributions using Seaborn plots.
4. Split the dataset into training (70%) and testing (30%) sets using `random_state=42`.
5. Standardize the features using `StandardScaler`, fitting only on training data.
6. Train a `LinearRegression` model.
7. Predict house prices and inspect residuals.
8. Evaluate predictions using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² score.
9. Save the trained regression model as `model.pkl` using Pickle and reload it for prediction.

## How to Run

1. Clone or download this repository.
2. Install the dependencies:

   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn notebook
   ```

3. Open the notebook:

   ```bash
   jupyter notebook house_price_prediction.ipynb
   ```

4. Run the notebook cells in order. The dataset is fetched by Scikit-learn, so an internet connection may be needed the first time it is downloaded.

> **Note:** The notebook also contains an optional Google Colab Drive-mount cell. Skip this cell when running locally. For future predictions, apply the same fitted `StandardScaler` used during training; `model.pkl` stores the regression model only.

## Evaluation

The notebook calculates:

- **MSE:** Average squared prediction error.
- **MAE:** Average absolute prediction error.
- **R²:** Proportion of variance explained by the model.

Actual metric values depend on running the notebook and are not hardcoded here.

## Generated Files

Running the notebook may generate `boxPlot.jpg`, `boxPlotTrain.jpg`, `boxPlotTestData.jpg`, and `model.pkl`.

## Future Improvements

- Compare Linear Regression with Random Forest and other regressors.
- Use cross-validation and hyperparameter tuning.
- Save the scaler alongside the model in a single preprocessing pipeline.
- Build a simple web interface for predictions.

## Author

**Gurman Singh**  
Computer Science student interested in Machine Learning, Python, and Artificial Intelligence.
ning and regression-based prediction.
