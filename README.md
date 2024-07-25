# Titanic_Dataset_Analysis
Data analysis on the Titanic dataset to explore factors affecting passenger survival, including data cleaning, exploratory data analysis, feature engineering, and predictive modeling.

# Data Analysis of Titanic Dataset

## Introduction

This project involves data analysis on the famous Titanic dataset. The analysis aims to understand the demographics and other characteristics of the passengers, and to determine what factors made people more likely to survive.

## Dataset

The dataset used in this project contains information about the passengers on the Titanic, including their age, sex, ticket class, fare, and whether they survived.

## Analysis

The analysis includes the following steps:

1. **Data Cleaning**: Handling missing values and converting data types.
2. **Exploratory Data Analysis (EDA)**: Visualizing and summarizing the main characteristics of the dataset.
3. **Feature Engineering**: Creating new features from existing data.
4. **Modeling**: Building predictive models to determine the likelihood of survival.

## Libraries Used

1. **Pandas**: For data manipulation and analysis.
2. **NumPy**: For numerical operations.
3. **Matplotlib** and **Seaborn**: For data visualization.
4. **Scikit-learn**: For building and evaluating machine learning models.

## Steps

1. **Data Cleaning**
   - Handle missing values.
   - Convert data types.

2. **Exploratory Data Analysis (EDA)**
   - Visualize the distribution of numerical and categorical features.
   - Explore relationships between features and the target variable (survival).

3. **Feature Engineering**
   - Create new features from existing data.
   - Transform features for better modeling.

4. **Modeling**
   - Split the data into training and testing sets.
   - Build and evaluate different machine learning models.
   - Select the best model based on performance metrics.

## Example Code

1. **Loading the Dataset**:
   ```python
   import pandas as pd

   df = pd.read_csv('titanic.csv')
   ```

2. **Data Cleaning**:
   ```python
   df['Age'].fillna(df['Age'].median(), inplace=True)
   df['Embarked'].fillna(df['Embarked'].mode()[0], inplace=True)
   ```

3. **Exploratory Data Analysis (EDA)**:
   ```python
   import seaborn as sns
   import matplotlib.pyplot as plt

   sns.countplot(x='Survived', data=df)
   plt.show()
   ```

4. **Modeling**:
   ```python
   from sklearn.model_selection import train_test_split
   from sklearn.ensemble import RandomForestClassifier
   from sklearn.metrics import accuracy_score

   X = df[['Pclass', 'Sex', 'Age', 'Fare']]
   X = pd.get_dummies(X, columns=['Sex'])
   y = df['Survived']

   X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
   model = RandomForestClassifier(n_estimators=100, random_state=42)
   model.fit(X_train, y_train)
   y_pred = model.predict(X_test)

   accuracy = accuracy_score(y_test, y_pred)
   print(f'Accuracy: {accuracy:.2f}')
   ```

## Conclusion

The project provides insights into the factors affecting the survival of Titanic passengers. It demonstrates the process of data cleaning, exploratory data analysis, feature engineering, and modeling in a real-world dataset.

---


## README.md

```markdown
# Data Analysis of Titanic Dataset

## Introduction

This project involves data analysis on the famous Titanic dataset. The analysis aims to understand the demographics and other characteristics of the passengers, and to determine what factors made people more likely to survive.

## Dataset

The dataset used in this project contains information about the passengers on the Titanic, including their age, sex, ticket class, fare, and whether they survived.

## Analysis

The analysis includes the following steps:

1. **Data Cleaning**: Handling missing values and converting data types.
2. **Exploratory Data Analysis (EDA)**: Visualizing and summarizing the main characteristics of the dataset.
3. **Feature Engineering**: Creating new features from existing data.
4. **Modeling**: Building predictive models to determine the likelihood of survival.

## Libraries Used

1. **Pandas**: For data manipulation and analysis.
2. **NumPy**: For numerical operations.
3. **Matplotlib** and **Seaborn**: For data visualization.
4. **Scikit-learn**: For building and evaluating machine learning models.

## Steps

1. **Data Cleaning**
   - Handle missing values.
   - Convert data types.

2. **Exploratory Data Analysis (EDA)**
   - Visualize the distribution of numerical and categorical features.
   - Explore relationships between features and the target variable (survival).

3. **Feature Engineering**
   - Create new features from existing data.
   - Transform features for better modeling.

4. **Modeling**
   - Split the data into training and testing sets.
   - Build and evaluate different machine learning models.
   - Select the best model based on performance metrics.

## Example Code

1. **Loading the Dataset**:
   ```python
   import pandas as pd

   df = pd.read_csv('titanic.csv')
   ```

2. **Data Cleaning**:
   ```python
   df['Age'].fillna(df['Age'].median(), inplace=True)
   df['Embarked'].fillna(df['Embarked'].mode()[0], inplace=True)
   ```

3. **Exploratory Data Analysis (EDA)**:
   ```python
   import seaborn as sns
   import matplotlib.pyplot as plt

   sns.countplot(x='Survived', data=df)
   plt.show()
   ```

4. **Modeling**:
   ```python
   from sklearn.model_selection import train_test_split
   from sklearn.ensemble import RandomForestClassifier
   from sklearn.metrics import accuracy_score

   X = df[['Pclass', 'Sex', 'Age', 'Fare']]
   X = pd.get_dummies(X, columns=['Sex'])
   y = df['Survived']

   X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
   model = RandomForestClassifier(n_estimators=100, random_state=42)
   model.fit(X_train, y_train)
   y_pred = model.predict(X_test)

   accuracy = accuracy_score(y_test, y_pred)
   print(f'Accuracy: {accuracy:.2f}')
   ```

## Conclusion

The project provides insights into the factors affecting the survival of Titanic passengers. It demonstrates the process of data cleaning, exploratory data analysis, feature engineering, and modeling in a real-world dataset.

## Requirements

1. **Python 3.x**
2. **Required Libraries**: List any additional libraries or dependencies needed to run the program.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/titanic-data-analysis.git
   ```

2. Navigate to the project directory:
   ```bash
   cd titanic-data-analysis
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Contribution

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

