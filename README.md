House Price Prediction Using Machine Learning
A beginner-friendly machine learning project that predicts California housing prices using Linear Regression. This project covers the basic machine learning workflow, including data exploration, preprocessing, model training, evaluation, and saving a trained model.

Author: Gurman Singh
Project Overview
The goal of this project is to understand how a regression model can learn relationships between housing characteristics and house prices. It uses the California Housing dataset provided by Scikit-learn.

The notebook includes exploratory data analysis (EDA), feature scaling, training a linear regression model, generating predictions, and measuring prediction errors.
Technologies Used
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab
- Pickle (model serialization)
Dataset
The dataset is loaded directly using sklearn.datasets.fetch_california_housing, so a separate CSV download is not required. Its input features are:
Feature	Description
MedInc	Median income in the area
HouseAge	Median house age
AveRooms	Average number of rooms
AveBedrms	Average number of bedrooms
Population	Population of the area
AveOccup	Average household occupancy
Latitude	Geographic latitude
Longitude	Geographic longitude


Target: Median house value, expressed in units of $100,000. These are district-level housing values, not individual home sale prices.
Project Workflow
1. Load the data: Fetch the California Housing dataset and convert it into a Pandas DataFrame.
2. Explore the data: Inspect records, summary statistics, missing values, and correlations.
3. Visualize the data: Create a pair plot and box plots to explore relationships and outliers.
4. Split the dataset: Use 70% of the data for training and 30% for testing (random_state=42).
5. Scale the features: Apply StandardScaler, fitting it on training data and transforming the test data.
6. Train the model: Fit a Scikit-learn LinearRegression model.
7. Make predictions: Predict housing values on the test set and analyze residuals.
8. Evaluate performance: Calculate Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² score.
9. Save the model: Serialize the trained regression model to model.pkl using Pickle and reload it for prediction.
Getting Started
1. Clone the repository
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
Replace YOUR_USERNAME and YOUR_REPOSITORY with your GitHub details.
2. Install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn notebook
3. Run the notebook
jupyter notebook house_price_prediction.ipynb
Run the notebook cells in order. The California Housing dataset may need to be downloaded on first use.

Note: The final cell mounts Google Drive in Google Colab. Skip that cell when running locally in Jupyter Notebook or VS Code.
Model Evaluation
The notebook evaluates predictions using:
- Mean Squared Error (MSE): Average squared prediction error; lower is better.
- Mean Absolute Error (MAE): Average absolute prediction error; lower is better.
- R² Score: Measures how much variation in the target is explained by the model; closer to 1 is generally better.
Run the evaluation cell to see the actual metric values. No benchmark scores are claimed here without verified notebook output.
Generated Files
Running the notebook saves the following files:
- boxPlot.jpg — Box plot of the original dataset.
- boxPlotTrain.jpg — Box plot of scaled training features.
- boxPlotTestData.jpg — Box plot of scaled testing features.
- model.pkl — Saved Linear Regression model.
These are generated outputs and do not need to be included in the repository for the notebook to run. The saved model.pkl contains the regression model only; the fitted scaler is not saved separately, so future input data must be transformed consistently before prediction.
Future Improvements
- Compare Linear Regression with Random Forest and other regression algorithms.
- Tune models using cross-validation.
- Save the fitted scaler alongside the model for easier reuse.
- Build a simple Streamlit interface for interactive predictions.
Author
Gurman Singh
Computer Science Student | Machine Learning & Python Enthusiast

This project was developed as a hands-on introduction to machine learning and regression-based prediction.
