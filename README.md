# Energy Output Predictions for a Combined Cycle Plant
This project uses various machine learning models to predict the energy output for a Combined Cycle Power Plant.

# Business Value
An accurate ML model can assist in forecasting and make the plant more efficient, reliable, and also save money.

# Data
The [data set](https://storage.googleapis.com/aipi_datasets/CCPP_data.csv) consists of 9,568 records of hourly readings for:
- Temperature (AT)
- Ambient Pressure (AP)
- Relative Humidity (RH)
- Exhuast Vacuum (V)
- Net Hourly electrical energy output (PE)

We use the other features to predict PE.

# Models and Methods
We create and test the following linear regression models:
- Linear Regression
- Linear Regression w/ LASSO
- Linear Regression w/ Ridge
- Degree 2 Polynomial Regression
- Degree 2 Polynomial Regression w/ Ridge
- Random Forest Regressor

We use repeated k-folds validation -- 5 folds, 2 repeats

# Evaluation
We value the RMSE output metric the most because it penalizes big errors, which at a power plant can cause blackouts and erode consumer trust.

We also capture MAE and R<sup>2</sup>.

# Results
The Random Forest has the best RMSE mean. It's a 22% improvement over the next best model, the degree 2 polynomial. The Random Forest model accounts for 96% of the variability in the Power Output.

# The Code
The code for visualizing the data and running the models is in the [Colab Sheet](ML_Foundations_Project_Repo.ipynb). The code is divided into sections and is also annotated for ease of understanding

# Before You Start
You will need to modify the **Load the Power Data** section to support a way to upload the data set. I used Google Drive, but you can also upload the file directly. The code to support both of these approaches is included in this section, but commented out.







