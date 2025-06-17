# UsedCarPricePrediction

## Project Overview
This project builds a machine learning model to predict used car prices based on a dataset of vehicle listings. The data was sourced from Kaggle (filename: `vehicles.csv`). The goal is to estimate the price of a used car using features like year, manufacturer, condition, odometer reading, and others.

---

## Dataset(https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data/data)
- **Filename:** `vehicles.csv`
- Contains over 350,000 listings with 26 columns including price, year, manufacturer, model, condition, and more.
- The dataset has many missing values and a wide range of categories, requiring cleaning and preprocessing.

---

## Data Preprocessing
- Selected key columns relevant for price prediction:
  - `price`, `year`, `manufacturer`, `condition`, `odometer`, `fuel`, `transmission`, `drive`, and `type`.
- Removed rows with missing values in these columns.
- Filtered listings to keep prices between $500 and $100,000 to remove outliers.
- Reduced categorical complexity by grouping rare manufacturers into an "Other" category.
- Applied one-hot encoding to categorical variables for model compatibility.

---

## Modeling
- Split data into training (80%) and testing (20%) sets.
- Trained a Linear Regression model to predict car prices.
- Evaluated performance with:
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - R² Score

---

## Results
- The model achieved a reasonable baseline performance with an MAE of about $6,200 and R² around 0.5.
- These results indicate the model explains roughly half of the price variance and has moderate prediction accuracy.

---

## Challenges
- Initial attempts to one-hot encode all categorical features failed due to memory errors caused by very high cardinality.
- Resolved by reducing features and grouping categories.
- Encountered empty dataset issues after filtering; fixed by carefully managing filtering and dropping missing data.

---

## Next Steps
- Experiment with more advanced algorithms such as Random Forest or Gradient Boosting.
- Perform additional feature engineering and data cleaning.
- Explore hyperparameter tuning to improve model accuracy.

---

## How to Run
1. Place `vehicles.csv` in your working directory.
2. Install required libraries:
  pip install numpy pandas matplotlib seaborn scikit-learn
3. Run the Jupyter notebook or Python script to train and evaluate the model.

---

## Contact
For questions or contributions, please contact mahatnitai@gmail.com.


