# Salary Prediction using Polynomial Regression

**Author:** Akshat Garg  

**Registration Number:** 23BCE10641 

**Application Number:** IN26011052

**Batch Number:** 1A

**Email ID:** akshat.23bce10641@vitbhopal.ac.in 

## Objective
The objective of this project is to build a Polynomial Regression model (Degree = 3) to predict employee salaries based on their position level, capturing the non-linear relationship between hierarchy and compensation.

## Dataset Link
- [Kaggle: Position Salaries Dataset](https://www.kaggle.com/datasets/akram24/position-salaries)

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `scikit-learn`
- `kaggle`

## Methodology
1. **Data Understanding**: Inspected the dataset, verified feature types, and confirmed `Level` as the input feature and `Salary` as the target variable.
2. **Data Preprocessing**: Checked for missing values and split the dataset into 80% training and 20% testing sets using `train_test_split`.
3. **Model Development**: Transformed `Level` using `PolynomialFeatures(degree=3)` and trained a `LinearRegression` model on the transformed features.
4. **Model Evaluation**: Evaluated performance using MAE, MSE, and $R^2$ score, along with a continuous polynomial regression curve overlay.

## Results
- **MAE:** 70,635.25
- **MSE:** 6,263,853,282.86
- **$R^2$ Score:** 0.8763

## Conclusion
Polynomial Regression (Degree 3) effectively models the non-linear relationship in the Position Salaries dataset ($R^2 \approx 0.8763$). While Linear Regression assumes a straight-line fit, Polynomial Regression incorporates higher-degree feature terms to fit exponential growth trends, making it well-suited for executive salary structures.