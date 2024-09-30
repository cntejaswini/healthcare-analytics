# Healthcare Analytics Project

This project is part of the Healthcare Analytics course, where we explore hospital inpatient data during the COVID-19 pandemic. The analysis includes preprocessing datasets, building predictive models to estimate hospital length of stay (HLOS), and conducting trials using both MLP and RNN models.

## Project Overview

The project consists of three key datasets:

1. **Data-at-admission**: Contains patient details and measurements taken at the time of admission.
2. **Days-breakdown**: Provides time-series data with daily vital signs and blood work results.
3. **Hospital-length-of-stay**: Tracks the length of stay in the hospital for each patient.

The goal is to predict the hospital length of stay (HLOS) for inpatients using the available features.

### Steps:

1. **Data Preprocessing**:
   - Dropped irrelevant columns and handled missing values using median imputation and KNN imputation.
   - Converted categorical variables (e.g., comorbidities, intubation status) into numerical form using encoding techniques like MultiLabelBinarizer and LabelEncoder.
   - Standardized numerical features using `StandardScaler`.

2. **Exploratory Data Analysis (EDA)**:
   - Performed summary statistics and visualized important features.
   - Identified key trends and patterns in the dataset.

3. **Modeling**:
   - **Multilayer Perceptron (MLP)**: Built an MLP model using `MLPRegressor` for HLOS prediction.
   - **Recurrent Neural Network (RNN)**: Built an RNN model using `SimpleRNN` and `LSTM` layers to capture the sequential nature of the data.

4. **Optimization**:
   - Ran multiple trials to find the best hyperparameters for both MLP and RNN models.
   - Evaluated model performance using Mean Squared Error (MSE) and R-squared metrics.

### Prerequisites

To run the project, you need to install the following dependencies:

- Python 3.x
- Required libraries: 
  ```bash
  pip install pandas matplotlib seaborn sklearn tensorflow openpyxl
  ```

### File Structure

- `Canada_Hosp1_COVID_InpatientData.xlsx`: The dataset containing three sheets: Data-at-admission, Days-breakdown, and Hospital-length-of-stay.
- `healthcare_analytics_project.ipynb`: The Jupyter Notebook containing the full implementation.
- `README.md`: This file, describing the project structure and how to run the analysis.

### How to Run

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd healthcare-analytics-project
   ```
3. Open the Jupyter notebook:
   ```bash
   jupyter notebook healthcare_analytics_project.ipynb
   ```

### Results

The project evaluates the following models:

- **MLP**: Achieved an average MSE of X over 5 trials.
- **RNN (LSTM)**: Achieved an average MSE of Y over 5 trials.

Both models are compared based on their predictive accuracy and computational performance.

### Future Work

- Experiment with additional models like GRU or Transformer-based architectures.
- Refine hyperparameters for better performance.
- Explore more advanced feature engineering techniques.

### License

This project is licensed under the MIT License.
