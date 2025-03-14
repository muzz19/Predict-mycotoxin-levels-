This project implements a machine learning pipeline to predict mycotoxin levels (DON concentration) in corn samples using hyperspectral imaging data. The pipeline includes data preprocessing, model training, hyperparameter tuning, and deployment.

Setup Instructions

Prerequisites

Ensure you have Python 3.8+ installed on your system. You can install the required dependencies using the following steps:

Installation

Clone the repository:

git clone <repository_url>
cd <repository_name>

Create a virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

Install dependencies:

pip install -r requirements.txt

Running the Code

Ensure that the dataset file (MLE-Assignment.csv) is in the project directory.

Run the main script to preprocess data and generate visualizations:

python main.py

Train and evaluate the model:

python train.py

Run the FastAPI application for serving predictions:

uvicorn app:app --host 0.0.0.0 --port 8000

Additional Notes

Ensure that the dataset is properly formatted before running the scripts.

Hyperparameter tuning can be performed using optuna with train.py.

The trained model can be loaded and used for inference via FastAPI.
