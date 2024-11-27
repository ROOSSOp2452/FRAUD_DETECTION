# FRAUD_DETECTION

This project aims to detect fraudulent transactions from a dataset containing various financial transactions. The dataset includes details about transactions like type, amount, and balances, along with a label indicating whether the transaction was fraudulent or not. The goal is to build a predictive model that can classify transactions as either "fraud" or "no fraud."

## Table of Contents
1. [Project Overview](#project-overview)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Data Preprocessing](#data-preprocessing)
5. [Model Training](#model-training)
6. [Evaluation](#evaluation)
7. [Visualizations](#visualizations)
8. [Contributing](#contributing)
9. [License](#license)

---

## Project Overview

The fraud detection system is built using machine learning algorithms, specifically using a **Decision Tree Classifier**, to identify fraudulent transactions based on transaction details like amount, type, and balance. The dataset used in this project is `Fraud.csv`, which contains a variety of transaction features.

Key metrics evaluated:
- **Precision**
- **Recall**
- **F1 Score**

---

## Installation

To run this project, you need to have Python installed along with the required libraries. You can install the dependencies using `pip`:

```bash
pip install -r requirements.txt
```

### Required Libraries:
- **pandas**
- **numpy**
- **matplotlib**
- **seaborn**
- **scikit-learn**
- **plotly**

---

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/fraud-detection.git
   cd fraud-detection
   ```

2. Ensure you have the dataset (`Fraud.csv`) available in the correct directory or update the file path in the script.

3. Run the main Python script:

   ```bash
   python fraud_detection.py
   ```

---

## Data Preprocessing

- **Loading the dataset**: The dataset is loaded using `pandas` from a CSV file.
- **Handling missing values**: Any rows with missing values are dropped.
- **Encoding categorical values**: The `type` column is encoded with numerical values using a custom mapping.
- **Feature selection**: Relevant features such as `type`, `amount`, and `newbalanceOrig` are selected for training the model.

---

## Model Training

- The dataset is split into training and testing sets using `train_test_split`.
- A **Decision Tree Classifier** is used to train the model to predict fraudulent transactions (`isFraud`).
- The model is then evaluated using metrics like precision, recall, and F1 score.

---

## Evaluation

The performance of the trained model is evaluated using the following metrics:

- **Precision**: Measures the accuracy of the positive predictions.
- **Recall**: Measures the ability of the model to identify all relevant positive cases.
- **F1 Score**: A balanced measure of precision and recall.

The following results are printed:

```bash
Precision Score: [value]
Recall Score: [value]
F1 Score: [value]
```

---

## Visualizations

Several visualizations are provided to help understand the data and model performance:
- **Heatmap of Correlations**: Displays correlations between numerical features in the dataset.
- **Fraud Detection Distribution**: Visualizes the distribution of fraud and non-fraudulent transactions.
- **Ribbon Graph with Scores**: A graphical representation that displays precision, recall, and F1 scores overlaid on a ribbon graph.

```python
# Example of visualizing the fraud distribution by transaction type
sns.countplot(data=df, x='type', hue='isFraud', palette='coolwarm')
```

---

## Contributing

Feel free to fork the project and submit pull requests for bug fixes, improvements, or new features. To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make changes and commit them (`git commit -am 'Add new feature'`).
4. Push to your fork (`git push origin feature-name`).
5. Open a pull request.

---


---

### Note:
Remember to modify the `requirements.txt` file with the list of libraries in use and ensure that the dataset path is correct before running the project.

Let me know if you need further changes!
