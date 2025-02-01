# Machine Learning Model Deployment with Flask

This repository demonstrates how to deploy a Machine Learning (ML) model using a Flask web application. The ML model in this project is built using a **Linear Regression** algorithm and is trained to predict employee salaries based on experience, test scores, and interview performance. The Flask app serves the model and provides an interface for users to input data and receive predictions.

## Project Overview

- **Model**: A simple Linear Regression model trained on a dataset containing features like years of experience, test scores, and interview scores.
- **Flask Application**: A lightweight Flask app serves the ML model to handle HTTP requests and provide predictions.
- **Pickle**: The model is serialized and saved using the `pickle` library for easy loading during inference.

## Dataset

The dataset used in this project is `hiring.csv`, which contains the following columns:
- **Experience**: The number of years of experience.
- **Test Score**: The score obtained in an aptitude test.
- **Interview Score**: The score obtained in the interview.
- **Salary**: The target variable representing the predicted salary.

## How It Works

1. **Data Preprocessing**: 
   - Missing values in the `experience` column are replaced with 0.
   - Missing values in the `test_score` column are filled with the mean value of the column.
   - The `experience` column, which contains textual data, is converted into numerical values using a dictionary lookup.

2. **Model Training**:
   - The dataset is split into features (X) and the target variable (y), and a **Linear Regression** model is trained on the entire dataset.

3. **Model Saving**:
   - The trained model is saved using `pickle` for later use in the Flask application.

4. **Model Deployment**:
   - The Flask app loads the trained model and serves an endpoint where users can input data and get salary predictions.

## Getting Started

### Prerequisites

- Python 3.x
- Flask
- Numpy
- Pandas
- Scikit-learn

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/lunatic-bot/Deployment-Demo.git
   cd ml-model-deployment-flask
2. Install the required Python libraries:

   ```bash
   pip install -r requirements.txt
3. Ensure that the hiring.csv file is available in the root directory, or update the path in the code.

### Acknowledgments
- OpenCV Documentation: https://docs.opencv.org/
- Flask Documentation: https://flask.palletsprojects.com/
- Scikit-learn Documentation: https://scikit-learn.org/

Feel free to explore, fork, and contribute to this repository!
