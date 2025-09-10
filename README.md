# Heart Disease Prediction API

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)](https://flask.palletsprojects.com/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A robust machine learning web service that leverages patient health data to predict cholesterol levels and assess cardiovascular risk factors. Built with Python, Flask, and Linear Regression algorithms to provide real-time predictions through RESTful API endpoints.

## 🚀 Features

- **Predictive Analytics**: Linear Regression model trained on 270+ patient records
- **RESTful API**: Clean, scalable endpoints for seamless integration
- **Data Visualization**: Comprehensive analysis with matplotlib and seaborn
- **Real-time Predictions**: Instant cholesterol level assessments
- **Feature Explanations**: Detailed insights into model parameters
- **Client Integration**: Ready-to-use Python client examples

## 🛠️ Technology Stack

| Category | Technologies |
|----------|-------------|
| **Backend** | Python, Flask |
| **Machine Learning** | scikit-learn, Linear Regression |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **API Testing** | Requests, JSON |
| **Development** | Jupyter Notebook |

## 📊 Dataset

The model utilizes the **Heart Disease Statlog Dataset** containing:
- **270+ patient records**
- **13 clinical features** (age, sex, chest pain type, blood pressure, etc.)
- **Target variable**: Cholesterol levels and heart disease presence

### Key Features:
- `age`: Patient age in years
- `sex`: Gender (0 = female, 1 = male)
- `cp`: Chest pain type (0-3)
- `trestbps`: Resting blood pressure
- `chol`: Serum cholesterol in mg/dl
- `thalach`: Maximum heart rate achieved
- `exang`: Exercise induced angina

## 🔧 Installation

### Prerequisites
- Python 3.8+
- pip package manager

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/heart-disease-prediction-api.git
   cd heart-disease-prediction-api
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Start the Flask server**
   ```bash
   python app.py
   ```

The API will be available at `http://127.0.0.1:5000`

## 📡 API Endpoints

### Base URL: `http://127.0.0.1:5000`

| Method | Endpoint | Description | Response |
|--------|----------|-------------|----------|
| `GET` | `/Heart/sample` | Retrieve sample patient data | JSON array of sample records |
| `GET` | `/Heart/explain` | Get feature explanations | Text description of model features |
| `POST` | `/Heart/evaluate` | Predict cholesterol levels | JSON with prediction results |

### Example Usage

#### Get Sample Data
```python
import requests

response = requests.get('http://127.0.0.1:5000/Heart/sample')
print('Sample Data:', response.json())
```

#### Make Prediction
```python
patient_data = {
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

response = requests.post('http://127.0.0.1:5000/Heart/evaluate', json=patient_data)
print('Prediction:', response.json())
```

## 📈 Model Performance

- **Algorithm**: Linear Regression
- **Training Data**: 270+ patient records
- **Features**: 13 clinical parameters
- **Accuracy**: Optimized for cholesterol level prediction
- **Validation**: Cross-validation techniques applied

## 🏗️ Project Structure

```
heart-disease-prediction/
│
├── Assignment2_Agambir_Singh_Part1.ipynb    # Data analysis & model training
├── Assignment2_Agambir_Singh_Part2.ipynb    # API client testing
├── Heart_disease_statlog.csv                # Dataset
├── app.py                                   # Flask API server
├── model.pkl                                # Trained ML model
├── requirements.txt                         # Python dependencies
└── README.md                               # Project documentation
```

## 🔍 Data Analysis Insights

The exploratory data analysis revealed:
- **Age Distribution**: Patients aged 29-77 years
- **Gender Balance**: 68% male, 32% female patients
- **Risk Factors**: Strong correlation between chest pain type and heart disease
- **Cholesterol Patterns**: Significant variation across age groups

## 🧪 Testing

Run the client notebook (`Assignment2_Agambir_Singh_Part2.ipynb`) to test all API endpoints:

1. **Sample Data Retrieval**: Validates API connectivity
2. **Feature Explanations**: Confirms model transparency
3. **Prediction Testing**: Verifies real-time prediction capability

## 🚀 Deployment Considerations

### Production Readiness
- [ ] Add authentication middleware
- [ ] Implement rate limiting
- [ ] Add comprehensive logging
- [ ] Set up monitoring and alerting
- [ ] Configure HTTPS/SSL
- [ ] Add input validation and sanitization

### Scaling Options
- **Docker**: Containerize for consistent deployment
- **Cloud Platforms**: AWS, GCP, or Azure deployment
- **Load Balancing**: Handle multiple concurrent requests
- **Database Integration**: Store predictions and user data

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Agambir Singh**
- LinkedIn: [Your LinkedIn Profile](https://linkedin.com/in/yourprofile)
- Email: your.email@domain.com
- Portfolio: [Your Portfolio Website](https://yourportfolio.com)

## 🙏 Acknowledgments

- Heart Disease Statlog Dataset contributors
- Sheridan College AI/ML Program
- Flask and scikit-learn communities
- Open source contributors

---

*Built with ❤️ for advancing healthcare through machine learning*
