# Heart Disease Prediction API

A machine learning web service that predicts cholesterol levels using patient health data. This project analyzes 270+ patient records and provides predictions through a simple REST API.

## What it does

This project uses Linear Regression to predict cholesterol levels based on patient information like age, blood pressure, chest pain type, and heart rate. The model is wrapped in a Flask API that healthcare applications can use to get real-time predictions.

## What I learned

- How to build and train machine learning models (use case of different algo.)
- Data visualization techniques and librarie such as matplot, seaborn etc.
- Creating REST APIs with Flask & Testing APIs with Python requests library
- End-to-end machine learning pipeline development from data preprocessig, training the models to deployment.
  

## Technology Stack

- **Python** - Main programming language
- **Flask** - Web framework for the API
- **scikit-learn** - Machine learning library
- **Pandas** - Data processing
- **Matplotlib & Seaborn** - Data visualization
- **Jupyter Notebook** - Development environment

## How to run

1. Install Python 3.8 or higher
2. Install required packages:
   ```bash
   pip install flask pandas scikit-learn matplotlib seaborn requests
   ```
3. Run the Flask server:
   ```bash
   python app.py
   ```
4. The API will be available at `http://127.0.0.1:5000`

## API Endpoints

- **GET /Heart/sample** - Returns sample patient data
- **GET /Heart/explain** - Explains what each feature means
- **POST /Heart/evaluate** - Predicts cholesterol level for given patient data

## Example Usage

```python
import requests

# Get sample data
response = requests.get('http://127.0.0.1:5000/Heart/sample')
print(response.json())

# Make a prediction
patient = {
    "age": 62,
    "sex": 0,
    "cp": 2,
    "trestbps": 130,
    "chol": 280,
    "restecg": 0,
    "thalach": 150,
    "exang": 1,
    "oldpeak": 2.5,
    "thal": 3
}

response = requests.post('http://127.0.0.1:5000/Heart/evaluate', json=patient)
print(response.json())
```

## Project Files

- `Assignment2_Agambir_Singh_Part1.ipynb` - Data analysis and model training
- `Assignment2_Agambir_Singh_Part2.ipynb` - API testing examples
- `Heart_disease_statlog.csv` - Dataset with patient records
- `README.md` - This file

## Dataset

The Heart Disease Statlog dataset contains information about 270+ patients with features like:
- Age, gender, chest pain type
- Blood pressure and cholesterol levels
- Heart rate and exercise test results
- ECG readings

This project demonstrates practical application of machine learning in healthcare, showing how data science can help predict health risks and support medical decision-making.
