# Student Scores Prediction Using Machine Learning

## Project Overview
This project analyzes the relationship between study hours and student exam scores. 
Several regression models are implemented and compared to evaluate their performance:
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

The dataset used is: student_scores.xlsx

---

## 1. Importing Libraries

The following libraries are used in this project:

- pandas → Data manipulation
- numpy → Numerical computation
- matplotlib → Data visualization
- seaborn → Statistical visualization
- scikit-learn → Machine learning models and evaluation

---

## 2. Data Loading

The dataset is loaded using pandas:

    data = pd.read_excel('student_scores.xlsx')

Initial inspection includes:
- data.head() → View first 7 rows
- data.info() → Dataset structure and data types
- data.describe() → Statistical summary

---

## 3. Data Visualization

### Scatter Plot
A pairplot is used to visualize the relationship between:
- Hours (x)
- Scores (y)

This helps to understand if a linear relationship exists.

### Outlier Detection
A boxplot is used to detect potential outliers in the Hours variable.

---

## 4. Data Cleaning

- Duplicate rows are checked using:
      df.duplicated()
- Duplicate rows are removed:
      df.drop_duplicates()
- Missing values are checked:
      df.isna().sum()

---

## 5. Feature Selection

- X (Independent Variable): Hours (x)
- Y (Dependent Variable): Scores (y)

---

## 6. Train-Test Split

The dataset is split into:
- 75% Training Data
- 25% Testing Data

Using:

    train_test_split(X, Y, train_size=0.75, random_state=42)

---

## 7. Linear Regression Model

### Training
    lr_model = LinearRegression()
    lr_model.fit(X_train, y_train)

### Evaluation
- R² Score
- Intercept
- Coefficient

Linear Equation Example:

    Y = 2.480 + 9.714x

Example calculation:
If study hours = 8.3

    Y = 2.480 + 9.714 * 8.3

The results are visualized by comparing:
- Actual values
- Predicted values

---

## 8. Decision Tree Regressor

### Training
    dt_model = DecisionTreeRegressor()
    dt_model.fit(X_train, y_train)

### Evaluation
- R² Score
- Visualization of actual vs predicted values

---

## 9. Random Forest Regressor

### Training
    model_rf = RandomForestRegressor()
    model_rf.fit(X_train, y_train)

### Evaluation
- R² Score
- Visualization of actual vs predicted values

---

## 10. Model Comparison

Each model is evaluated using:
- R² Score (Coefficient of Determination)

Higher R² indicates better model performance.

Models compared:
1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor

---

## Conclusion

This project demonstrates:
- Data preprocessing and cleaning
- Exploratory data analysis
- Regression model training
- Model evaluation and comparison

Linear Regression works well when the relationship is linear.
Decision Tree and Random Forest can capture more complex patterns.

---

## How to Run

1. Place student_scores.xlsx in the same directory.
2. Install required libraries:

    pip install pandas numpy matplotlib seaborn scikit-learn openpyxl

3. Run the Python script.

---

Author: Muhammad Auffa Hakim Aditya
Student Machine Learning Practice Project
