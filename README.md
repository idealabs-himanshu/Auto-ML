# h2o_automl_app

This project provides a command-line interface and Streamlit-based web application for building and deploying H2O AutoML models in Python.

## Key Features

- Train supervised machine learning models on a local dataset
- Train regression, classification, or unsupervised anomaly detection models
- Evaluate model performance using key metrics like accuracy, F1-score, and AUC
- Visualize model performance through interactive plots
- Manage models by saving, loading, and deleting them
- Deploy trained models to predict on new unseen data

## Prerequisites and Installation

### Python Environment
- Python 3.8 or later

### Required Packages
- json
- datetime
- streamlit
- shutil
- pandas
- h2o
- traceback
- plotly

### Installation

1. Clone the repository.
```
git clone https://github.com/username/h2o_automl_app.git
```

2. Install the required packages.
```
pip install -r requirements.txt
```

## Usage Instructions

### Command-Line Interface

The command-line interface provides basic functionality for training and managing models. Run the following command to access the interface:
```
python main.py
```

### Streamlit Application

The Streamlit application provides a user-friendly interface for training, managing, and visualizing models. Run the following command to launch the application:
```
streamlit run main.py
```

## Project Structure

- **h2o_automl_app**: Main project directory
 - **main.py**: Entry point for both the command-line interface and Streamlit application
 - **utils.py**: Contains helper functions used throughout the project

## Functions

- **init_h2o()**: Initializes the H2O cluster.
- **validate_model_name(model_name)**: Validates the given model name.
- **delete_model(model_name)**: Deletes the specified model.
- **describe_model_performance(model)**: Prints a summary of the model's performance.
- **analyze_column_types(df)**: Analyzes the data types of the columns in the given DataFrame.
- **create_visualizations(model, X_test, y_test)**: Creates interactive plots to visualize model performance.
- **manage_models()**: Provides options to save, load, and delete models.
- **train_model(train_data_path, model_name, target_column, **kwargs)**: Trains a model using H2O AutoML.
- **predict(model_name, input_data_path, output_path, target_column)**: Makes predictions using a trained model.
- **main()**: Main function that orchestrates the project's functionality.
