# Titanic Survival Classification

## Project Goal

The goal of this project is to build a machine learning classification model that predicts whether a Titanic passenger survived or not.

The model uses passenger information such as class, sex, age, number of family members, fare, and embarkation location.

## Dataset

This project uses the Titanic dataset.

Main columns include:

```text
PassengerId, Survived, Pclass, Name, Sex, Age, SibSp, Parch, Ticket, Fare, Cabin, Embarked
```

Target column:

```text
Survived
```

Where:

```text
0 = Did not survive
1 = Survived
```

## Project Workflow

This project follows a basic machine learning workflow:

1. Load the dataset
2. Explore the data
3. Check missing values
4. Clean the dataset
5. Select useful features
6. Convert categorical features into numeric format
7. Split the data into training and testing sets
8. Train classification models
9. Evaluate model performance
10. Compare model results

## Data Cleaning

The dataset had missing values in important columns.

Cleaning steps:

- Filled missing `Age` values with the median age
- Filled missing `Embarked` values with the most common value
- Dropped the `Cabin` column because it had too many missing values

## Features Used

The selected input features were:

```text
Pclass, Sex, Age, SibSp, Parch, Fare, Embarked
```

The target variable was:

```text
Survived
```

Categorical columns such as `Sex` and `Embarked` were converted into numeric columns using one-hot encoding.

## Models Used

Two machine learning models were trained and compared:

1. Logistic Regression
2. Decision Tree Classifier

## Model Results

| Model | Accuracy |
|---|---:|
| Logistic Regression | 81% |
| Decision Tree Classifier | 78% |

## Key Findings

- Logistic Regression performed better than the Decision Tree Classifier.
- Logistic Regression achieved an accuracy of about 81%.
- Decision Tree Classifier achieved an accuracy of about 78%.
- The model performed slightly better at predicting passengers who did not survive.
- Features such as sex, passenger class, age, and fare were useful for survival prediction.

## Project Structure

```text
titanic-survival-classification/
├── data/
│   ├── raw/
│   │   └── Titanic-Dataset.csv
│   └── processed/
├── notebooks/
│   └── model.ipynb
├── README.md
└── requirements.txt
```

## Tools Used

- Python
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- Jupyter Notebook
- Git and GitHub

## How to Run

Install the required packages:

```bash
pip install -r requirements.txt
```

Open the notebook:

```bash
jupyter notebook
```

Then run:

```text
notebooks/model.ipynb
```

## What I Learned

In this project, I practiced:

- loading and exploring a dataset with pandas
- handling missing values
- selecting features for machine learning
- encoding categorical variables
- splitting data into train and test sets
- training classification models
- evaluating models with accuracy, confusion matrix, and classification report
- comparing multiple machine learning models

## Next Improvements

Possible improvements for this project:

- Add more feature engineering, such as family size
- Try Random Forest or Gradient Boosting
- Tune model hyperparameters
- Visualize feature importance
- Save the trained model using `joblib`
