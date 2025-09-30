# Linear Regression

This project explores the fundamentals of linear regression using Scikit-learn, covering basic model fitting, data generation, and a practical application on the diabetes dataset. The solutions are implemented in the following Jupyter Notebooks:

- `ex01_estimator.ipynb`: Covers the basics of Scikit-learn estimators, 1D linear regression, and train-test splitting.
- `forecast.ipynb`: Applies linear regression to forecast diabetes progression.

---

## `ex01_estimator.ipynb`: Core Concepts

This notebook introduces the core mechanics of linear regression.

### 1. Basic Estimator

- A simple `LinearRegression` model is fitted on a small, 2D dataset (`X, y = [[1], [2.1], [3]], [[1], [2], [3]]`).
- The model's coefficients, intercept, and score are printed.
- A prediction is made for a new data point (`x_pred = [[4]]`), resulting in `y_pred = 3.96`.

### 2. 1D Linear Regression

- **Data Generation**: A dataset is generated using `make_regression` with 100 samples and a noise level of 10.
- **Model Fitting**: A linear regression model is fitted to this data. The resulting equation is `y = 42.62 * x + 99.19`.
- **Visualization**: The raw data points and the fitted regression line are plotted, showing a clear linear relationship.
- **Error Calculation**: The Mean Squared Error (MSE) is calculated to be **114.17**.
- **Impact of Noise**: The experiment is repeated with a higher noise level of 50. This results in a much higher MSE of **2854.29**, demonstrating that increased noise makes it harder for the model to find the underlying pattern.

### 3. Train-Test Split

- The notebook demonstrates how to split a dataset into training (80%) and testing (20%) sets using `train_test_split`. This is a crucial step for evaluating a model's performance on unseen data.

---

## `forecast.ipynb`: Diabetes Progression Forecast

This notebook applies linear regression to a real-world dataset to predict the progression of diabetes.

### 1. Data Preparation

- The `load_diabetes` dataset from Scikit-learn is used.
- The data is split into a training set and a testing set (20% of the data) to evaluate the model's performance.

### 2. Model Training and Prediction

- A `LinearRegression` model is trained on the training data.
- The model's coefficients and intercept are extracted to form the final regression equation.
- The trained model is used to make predictions on the test set.

### 3. Performance Evaluation

- The Mean Squared Error (MSE) is calculated for both the training and testing sets to assess the model's accuracy.
- **Train MSE**: `2888.32`
- **Test MSE**: `2858.29`

The similar MSE on the train and test sets suggests that the model is generalizing well and not overfitting to the training data.

## Usage

To run the notebooks in this repository:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/stkisengese/linear-regression.git
    cd linear-regression
    ```
2.  **Create and activate a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```
3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Launch Jupyter Lab or Jupyter Notebook:**
    ```bash
    jupyter lab
    # or
    jupyter notebook
    ```
    This will open a browser window where you can navigate to and run `ex01_estimator.ipynb` and `forecast.ipynb`.

## License

This project is licensed under the terms of the [MIT LICENSE](LICENSE) file.
