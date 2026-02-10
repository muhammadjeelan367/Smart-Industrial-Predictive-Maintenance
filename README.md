# Machine Predictive Maintenance Classification
This repository hosts a machine predictive maintenance classification project, aimed at predicting the maintenance needs of industrial machinery before they fail. By leveraging machine learning algorithms, this project seeks to enhance operational efficiency and reduce downtime by identifying potential maintenance requirements proactively.

## Dataset

The dataset utilized in this project comprises historical data collected from sensors embedded in industrial machinery. It includes various operational parameters such as 'Type', 'Air temperature [K]','Process temperature [K]', 'Rotational speed [rpm]', 'Torque [Nm]',
'Tool wear [min]', 'Target', and other performance metrics. Additionally, maintenance records indicating when maintenance was performed and the type of maintenance conducted are included. This dataset enables the development of predictive models to classify whether a machine requires maintenance within a certain time frame.

## Project Structure

The project structure is organized as follows:

- **data:** Contains the dataset used for training and testing the predictive models.
- **notebooks:** Includes Jupyter notebooks detailing the data preprocessing steps, feature engineering, model development, and evaluation.
- **src:** Houses any source code or utility functions utilized in the project, such as custom preprocessing scripts or model implementations.
- **reports:** Contains reports generated from the analysis, including visualizations, model performance metrics, and insights.

## Data Preprocessing and Feature Engineering

Data preprocessing is a crucial step in preparing the dataset for predictive modeling. It involves handling missing values, scaling features, encoding categorical variables, and possibly removing outliers. Additionally, feature engineering may be performed to create new features or transform existing ones to improve model performance and capture relevant patterns in the data.

Key aspects of data preprocessing and feature engineering include:

- Handling missing data
- Scaling numerical features
- Encoding categorical variables
- Feature selection
- Engineering new features based on domain knowledge

## Predictive Maintenance Classification

The primary task of this project is to develop predictive models capable of classifying whether a machine will require maintenance within a certain time frame. Various machine learning algorithms such as logistic regression, decision trees, random forests, gradient boosting, or neural networks may be explored and evaluated for their predictive performance.

The predictive maintenance classification involves:

- Data splitting into training and testing sets
- Model training using different algorithms
- Hyperparameter tuning for optimizing model performance
- Model evaluation using appropriate metrics such as accuracy, precision, recall, F1-score, and ROC-AUC curve

## Getting Started

To get started with this project, follow these steps:

1. Clone this repository to your local machine.
2. Navigate to the `notebooks` directory to explore the Jupyter notebooks containing the analysis and modeling process.
3. Ensure you have the necessary dependencies installed. You can install them via pip using the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

4. Run the notebooks sequentially to replicate the analysis and understand the steps involved.

## Requirements

The project requires Python 3.11 along with various libraries such as pandas, numpy, matplotlib, seaborn, scikit-learn, tqdm etc. These dependencies are listed in the `requirements.txt` file.

## Contributing

Contributions to this project are welcome. If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.

Please customize this README according to your project's specific details and preferences.
