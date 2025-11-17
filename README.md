# Salary Classification and Fairness Analysis

This project evaluates the performance of a binary salary classification model across different demographic groups. Using Python and scikit-learn, I compare metrics such as precision, recall, and F1-score to identify potential fairness concerns.

## Project Overview

The notebook:

1. Loads salary test data split by demographic groups (e.g., male/female, racial categories).
2. Applies a pre-trained salary classifier loaded from a `.model` file.
3. Computes accuracy and detailed classification reports for each group.
4. Interprets the metrics to discuss where the model may be underperforming or potentially biased.

## Data

The data consists of CSV files with features such as:

- `age`
- `education-num`
- `marital-status`
- `occupation`
- `relationship`
- `race`
- `sex`
- `native-country`
- `y` – target label indicating whether income is above or below a threshold

Files (stored in `data/`):

- `salary_test_data_male.csv`
- `salary_test_data_female.csv`

> Note: File names and data structure are based on a course lab. Datasets are included only for educational purposes.

## Methods

Key steps:

1. **Featurization**
   - Select a subset of informative columns (age, education, etc.)
   - Encode categorical fields such as `marital-status` into numeric features

2. **Model Inference**
   - Load a pre-trained salary classifier from a `.model` file using `pickle`
   - Generate predictions for each demographic group

3. **Evaluation**
   - Calculate `accuracy_score`
   - Use `classification_report` to obtain precision, recall, and F1-score
   - Compare performance across groups

4. **Fairness Discussion**
   - Identify which groups have lower F1-scores or recall
   - Discuss potential implications for fairness and bias
   - Highlight limitations of dataset and model

## Technologies Used

- **Language:** Python
- **Libraries:**
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `pickle`
- **Tools:** Jupyter Notebook / Google Colab

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/salary-classification-fairness-analysis.git
   cd salary-classification-fairness-analysis
