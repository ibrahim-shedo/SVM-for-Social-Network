# SVM Classification on Customer Purchase Dataset

## Overview
This project utilizes Support Vector Machine (SVM) algorithms to classify customer purchasing behavior based on demographic and financial attributes. The dataset contains information about customers, including their age, estimated salary, and whether they made a purchase.

## Dataset

### Description
The dataset consists of customer records with the following features:

| Feature             | Type        | Description                                            |
|---------------------|-------------|--------------------------------------------------------|
| User ID             | Integer     | Unique identifier for each customer                   |
| Gender              | Categorical | Gender of the customer (Male/Female)                  |
| Age                 | Integer     | Age of the customer                                    |
| Estimated Salary     | Integer     | Estimated annual salary of the customer               |
| Purchased           | Binary      | Indicator of purchase (0 = Not Purchased, 1 = Purchased) |

### Sample Data
| User ID | Gender | Age | Estimated Salary | Purchased |
|---------|--------|-----|------------------|-----------|
| 15624510| Male   | 19  | 19000            | 0         |
| 15810944| Male   | 35  | 20000            | 0         |
| 15668575| Female | 26  | 43000            | 0         |
| 15603246| Female | 27  | 57000            | 0         |
| 15804002| Male   | 19  | 76000            | 0         |

## Methodology

### Data Preprocessing
1. **Data Cleaning**: The dataset was inspected for missing or inconsistent data.
2. **Feature Encoding**: Categorical features (Gender) were encoded to numerical format for model compatibility.
3. **Feature Scaling**: StandardScaler was used to normalize feature values, improving the SVM performance.

### SVM Model
Multiple SVM kernels were tested for classification:

1. **Linear Kernel**: A straightforward approach to classify data with a linear decision boundary.
2. **RBF Kernel**: A radial basis function kernel that can model non-linear relationships in the data.
3. **RBF Kernel with Specific Parameters**: Setting `gamma=15` and `C=7` to fine-tune the model's performance.
4. **Polynomial Kernel**: Explores polynomial relationships between features.

### Model Training and Evaluation
- The dataset was split into training and testing sets.
- The SVM models were trained on the training set, and predictions were made on the test set.
- The accuracy of each model was evaluated using accuracy metrics.

## Results
- The accuracy of each kernel was recorded to assess their effectiveness in classifying customer purchases.
- Visualizations of decision boundaries were created to illustrate how well each model separates the classes.

## Usage
To replicate this analysis, clone the repository and follow the steps below:
1. Install the required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib
Run the provided Jupyter Notebook or Python script to execute the SVM classification and view the results.
Conclusion
This project demonstrates the application of SVM in a classification problem and illustrates how different kernels can affect model performance. The results indicate the potential of SVM for predicting customer purchasing behavior based on demographic and financial features.
