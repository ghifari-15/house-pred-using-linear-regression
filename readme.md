# House Price Prediction Based on Area Statistics

This project aims to predict house prices based on area statistics using a linear regression model. The dataset contains information about average area income, house age, number of rooms, number of bedrooms, area population, house price, and address.

## Project Structure

```
readme.md
data/
    dataset.csv
src/
    index.ipynb
```

- **`data/dataset.csv`**: The dataset used for analysis and model training.
- **`src/index.ipynb`**: Jupyter Notebook containing code for data analysis, visualization, model training, and evaluation.

## Project Features

1. **Data Analysis**:
   - Display dataset information (`df.info()`).
   - Descriptive statistics (`df.describe()`).
   - Visualize feature distributions and relationships.

2. **Data Preprocessing**:
   - Remove missing values (`df.dropna()`).
   - Separate features and target for model training.

3. **Visualization**:
   - Pairplot to observe relationships between features.
   - Heatmap to analyze feature correlations.
   - Histogram for house price distribution.

4. **Modeling**:
   - Use linear regression to predict house prices.
   - Evaluate the model using metrics such as MAE, MSE, RMSE, and R².

5. **Prediction**:
   - Predict house prices based on new data.

## How to Run the Project

1. **Environment Setup**:
   - Ensure Python and Jupyter Notebook are installed.
   - Install required libraries:
     ```bash
     pip install pandas numpy seaborn matplotlib scikit-learn
     ```

2. **Run the Notebook**:
   - Open the `src/index.ipynb` file using Jupyter Notebook.
   - Execute each cell to perform analysis, train the model, and make predictions.

## Dataset

The dataset contains 5000 rows with the following columns:
- `Avg. Area Income`: Average income of the area.
- `Avg. Area House Age`: Average age of houses in the area.
- `Avg. Area Number of Rooms`: Average number of rooms in houses.
- `Avg. Area Number of Bedrooms`: Average number of bedrooms in houses.
- `Area Population`: Population of the area.
- `Price`: House price.
- `Address`: Address of the house.

## Model Results

The linear regression model produces the following evaluation metrics:
- **Mean Absolute Error (MAE)**: Average absolute error.
- **Mean Squared Error (MSE)**: Average squared error.
- **Root Mean Squared Error (RMSE)**: Square root of MSE.
- **R² Score**: Coefficient of determination to measure model performance.

## Predicting New Data

Example of predicting house prices based on new data:
```python
new_data = pd.DataFrame({
    'Avg. Area Income': [74568.64],
    'Avg. Area House Age': [5.182],
    'Avg. Area Number of Rooms': [7.62],
    'Avg. Area Number of Bedrooms': [4.09],
    'Area Population': [25045.34],
})

new_predictions = lm.predict(new_data)
print(f"Predicted Price for new data: {new_predictions[0]:.0f}")
```

## License

This project is licensed under the [MIT License](LICENSE).