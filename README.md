# Predicting Students Mathematics Performance using Machine Learning Models

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [Data Preprocessing](#data-preprocessing)
- [Data analysis](#data-analysis)
- [Model evaluation](#model-evaluation)
- [Results](#results)
- [Variable importance](#variable-importance)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

### Project Overview
---

This projects aims to predict students Mathematic performance using different machine learning models. By comparing the performnace of the various machine learning models, we seek to identify the model with the best predictive performance to predict students mathematics performance. This will help to earlier identification of students who are likely to perform poorly in mathematics based on their characteristics and provide them with the needed support as quick as possible. 

### Data Sources

The data for this project is the "GP_school_data.csv" file containing data on students scores in Mathematics as well as their demographics, family, and school characteristics. A detailed description of the variables can be found in the [article written by Paulo Cortez and Alice Silva](https://repositorium.uminho.pt/bitstream/1822/8024/1/student.pdf).

### Tools 

- RStudio - Data Cleaning and Manipulation
- Python - Building Machine Learning Models

### Data Cleaning

During the initial preparation of the data, we performed the tasks below:
- Data Loading and inspection in Rstudio
- Checking for missing data in tne variables of interest
- Renaming variables
- creating dummy variables for the categorical predictors
- Finally, exporting the data in "csv" format to be analysed using Python Programming Software

### Data Preprocessing

The "csv" file was imported in Python and the following tasks were performed:
- Creating three seperate datasets for each target variable (i.e., continuous, binary, and ordinal) by following the guidelines in the [Paulo Cortez and Alice Silva](https://repositorium.uminho.pt/bitstream/1822/8024/1/student.pdf).
- Splitting the data into testing and training datasets
- Standardizing the continuous features in the testing and training datasets seperately to prevent any information leakage from the testing to the training data.
- For the datasets with binary and ordinal outcomes, SMOTE was employed to handle class imbalances.
- Three separate notebooks were created for the three datasets, namely:
   - "math_continuous.ipynb" for modelling the data with continuous outcome variable
   - "math_binary.ipynb" for modelling the data with binary outcome variable
   - "math_multicategorical.ipynb" for modelling the data with multicategorical outcome variable

### Data analysis

To predict students mathematics performance, the eight machine learning models below were utilzed:
- Linear regression (for the continuous target variable) and logistic regression (for the ordinal and binary target variables)
- Decision Tree
- Random Forest
- Gradient Boosting
- Support Vector Machine
- Lasso regression
- Ridge regression
- Elastic Net regression

### Model evaluation

The models were evaluated using the following metrics:
- R-square values were used to evaluate the predictive performance of the models in the analysis of the data with continuous target variable.
- Sensitivity, Specificity, and Accuracy metrics were used to evaluate predictive performance of the models in the analysis of the data with binary target variable.
-  Accuracy metric was used to evaluate predictive performance of the models in the analysis of the data with multicategorical target variable.


### Results

- The Decision Tree algorithm produced the highest predictive performance (i.e., R_squared value) in the analysis  of the data with continuous outcome
- For the analysis of the data with binary target variable, the Support Vector Machine algorithm yielded the best performance accross all three evaluations metrics, namely:
  - Sensitivituy
  - Specificity
  - Accuracy
- Similarly, the Support Vector Machine algorithm yielded the best performance (;e., the highest accuracy) in the analysis of the data with multicategorical target variable

<img width="1000" height="600" alt="Model performance (continuous target variable)" src="https://github.com/user-attachments/assets/b832eba0-0685-4b1d-84e0-601594511f77" />

<img width="1200" height="600" alt="Model performance (binary target variable)" src="https://github.com/user-attachments/assets/f59e5983-aadd-4e62-b532-56ff215b97c9" />

<img width="1000" height="600" alt="Model performance (multicategorical target variable)" src="https://github.com/user-attachments/assets/1fb0b385-9332-4267-b49e-6998dd430355" />

### Variable importance

By examining variable importance in models such as the Decision tree, Random forest, Lasso, Ridge, and Elastic Net, the following variables showed up as the most important variables in predicting students mathematics performance:
- First period grade
- Second period Grade
- Number of school absences
- Age
- Number of past class failures
- Quality of family relationship

### Recommendations

- Students data should be modelled in early stages of the semester to identify students who are likely to struggle with mathematics performance.
- Adequate additional support should be provided to the identified students.
- Efforts should be made to increase school attendance
- Family members should be trained on how best they can support their children to improve their Mathematics performance.

### Limitations

The sample size for the analysis was relatively small. This can affect the generalizability of the findings. There are other important predictors including the characteristics of the mathematics treachers, that were not captured in the data. Some of these caharacteristics include teacher's years of experience, teacher's level of education, etc. These are important variables that can help predict the peromance of students in mathematics. Therefore, new studies should consider capturing data on teacher characteristics in addition to student and school characteristics.  

### References

1. [SKlearn]([scikit-learn: machine learning in Python — scikit-learn 1.7.1 ...](https://scikit-learn.org/stable/)
2. Hastie, T., Tibshirani, R., & Friedman, J. (2009). An introduction to statistical learning.
3. Silva, A. (2008). Using data mining to predict secondary school student performance.
   









