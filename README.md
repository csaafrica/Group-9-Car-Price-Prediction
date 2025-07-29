# Car Price Prediction Case Study

## Objective

You are a Data Scientist tasked with building a data-driven pricing model for a car dealership. Your goal is to:

- Clean and preprocess the raw data
- Perform exploratory data analysis (EDA)
- Visualize important insights
- Build a machine learning model to predict car prices

> **Note:** You are expected to identify key assumptions and draw actionable insights yourself as part of your final report.

## Dataset Overview

The dataset contains the following columns:

- **price:** Selling price of the car (target variable)
- **transmission:** Gearbox type (e.g., Automatic, Manual)
- **condition:** Vehicle condition (e.g., Foreign Used)
- **mileage:** Distance the vehicle has been driven (in km)
- **Name:** A combined string of manufacturer, model, year, engine, and color (e.g., `Toyota Premio 2015 1.8 FWD Black`)

## Part 1: Data Cleaning and Preprocessing

**Tasks:**

1. **Split the Name column** into:
   - `make` (e.g., Toyota)
   - `model` (e.g., Premio)
   - `year` (e.g., 2015)
   - `engine_info` (e.g., 1.8 FWD)
   - `color` (e.g., Black)
2. Handle missing values, if any.
3. Convert `year` to numeric and ensure all other fields are correctly typed.
4. Create a new feature:
   - `car_age = Current Year (e.g., 2024) - year`
5. Normalize or encode categorical features appropriately (e.g., one-hot encoding).

## Part 2: Exploratory Data Analysis (EDA)

**Tasks:**

1. Identify the most common car brands and models.
2. Analyze the distribution of car prices.
3. Compare how mileage varies across car brands.
4. Explore the relationship between car age, mileage, and price.
5. Check for price differences between transmission types.

## Part 3: Data Visualization and Storytelling

**Tasks:**

1. Plot a histogram of car prices.
2. Use a boxplot to compare price across transmission types.
3. Create a scatter plot of mileage vs. price, colored by car condition.
4. Generate a bar chart of average price per brand.
5. Produce a correlation heatmap (after preprocessing) for numerical features.

## Part 4: Model Building

**Tasks:**

1. Split the dataset into training and test sets.
2. Train a regression model (e.g., Linear Regression, Random Forest Regressor) to predict price.
3. Evaluate the model using MAE, RMSE, and R².
4. Identify the top 5 features influencing price using feature importance.

---

