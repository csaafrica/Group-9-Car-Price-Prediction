Car Price Prediction Model

This project is a data-driven case study to predict the selling price of used cars. Using a dataset of car details, we perform comprehensive data cleaning, exploratory data analysis (EDA), feature engineering, and predictive modeling.

The primary goal is to build a regression model that accurately estimates car prices based on features like mileage, transmission, condition, make, model, and car_age.

Table of Contents

    Project Overview

    Dataset

    Methodology

        1. Data Cleaning & Preprocessing

        2. Exploratory Data Analysis (EDA)

        3. Feature Engineering

        4. Model Building & Evaluation

    Key Findings & Results

    Technologies Used

    How to Run This Project

    Contributors

Project Overview

The objective of this project is to develop a robust pricing model for a car dealership. By analyzing historical sales data, we identify the key factors that influence a car's price. The final output is a machine learning model trained to predict prices, which can help the dealership optimize its pricing strategy.

The full analysis and model development process is available in the data_model2.ipynb notebook.

Dataset

The dataset (CarPrice.csv) contains the following columns:

    price: Selling price of the car (Target Variable)

    transmission: Gearbox type (e.g., Automatic, Manual)

    condition: Vehicle condition (e.g., Foreign Used)

    mileage: Distance the vehicle has been driven (in km)

    Name: A combined string of manufacturer, model, year, engine, and color.

Methodology

The project followed a structured data science workflow:

1. Data Cleaning & Preprocessing

    Parsed the Name column: Split the single string into new, usable features: make, model, year, engine_info, and color.

    Handled Missing Values: Implemented strategies to manage any missing data to ensure model stability.

    Corrected Data Types: Converted year and price to numeric types for calculation.

2. Exploratory Data Analysis (EDA)

    Analyzed the distribution of car prices to understand the target variable.

    Identified the most common car brands and models in the dataset.

    Explored relationships between key features (like mileage, car_age, and transmission) and the price.

3. Feature Engineering

    Created car_age: Engineered a new feature by subtracting the year from the current year (e.g., 2024), which is often more predictive than the manufacturing year itself.

    Encoded Categorical Features: Converted categorical columns like transmission, condition, and make into a numerical format (e.g., One-Hot Encoding) for the model.

4. Model Building & Evaluation

    Split the Data: The dataset was divided into training and testing sets (e.g., 80% train, 20% test) to evaluate the model's performance on unseen data.

    Trained Regression Models: Implemented and compared multiple regression algorithms (e.g., Linear Regression, Random Forest Regressor, Gradient Boosting).

    Evaluated Performance: Assessed the models using standard regression metrics.

Key Findings & Results

After training and evaluation, the Random Forest Regressor was selected as the best-performing model.

    Model Performance:

        R-squared (R²): 0.9327

        Mean Absolute Error (MAE): 157097.3990

        Root Mean Squared Error (RMSE): 688122.8292

    Top 4 Features Influencing Price:

        Feature 1, engine_size

        Feature 2, car_age

        Feature 3, car model

        Feature 4, mileage


    Key Insight: The analysis showed that car age and engine size are the strongest predictors of price, with premium model cars commanding a significant price premium over other brands counterparts.

Technologies Used

    Python

    Pandas: For data manipulation and analysis.

    NumPy: For numerical operations.

    Matplotlib & Seaborn: For data visualization.

    Scikit-learn (sklearn): For data preprocessing, feature engineering, and machine learning modeling.

    Jupyter Notebook: For interactive development and analysis.

How to Run This Project

    Clone the repository:
    Bash

git clone https://github.com/csaafrica/Group-9-Car-Price-Prediction.git
cd Group-9-Car-Price-Prediction

Create a virtual environment (Recommended):
Bash

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

Install the required libraries:
Bash

pip install -r requirements.txt

Launch Jupyter Notebook:
Bash

    jupyter notebook

Contributors

    Max Kinyua - Team Lead

    Vallarie Wakhula

    Angelica Ogato