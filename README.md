# BishSen
bish.ai an sentimental analysis platform regards all ml conspiracies.
### Endpoints

#### 1. Home
```bash
GET /
```

#### 2. Health Check
```bash
GET /health
```

#### 3. Model Info
```bash
GET /model-info
```

#### 4. Make Prediction
```bash
POST /predict
Content-Type: application/json

{
  "age": 35,
  "gender": "Male",
  "tenure_months": 24,
  "monthly_charges": 75.5,
  "total_charges": 1800.0,
  "contract_type": "One year",
  "payment_method": "Credit card",
  "internet_service": "Fiber optic",
  "online_security": "Yes",
  "tech_support": "Yes",
  "num_services": 5,
  "customer_service_calls": 2
}
```

**Response:**
```json
{
  "prediction": "NO CHURN",
  "churn_probability": 0.23,
  "retention_probability": 0.77,
  "risk_level": "LOW"
}
```

## 🧪 Testing the API

### Using cURL
```bash
curl -X POST http://localhost:5000/predict \
  -H "Content-Type: application/json" \
  -d '{
    "age": 45,
    "gender": "Female",
    "tenure_months": 60,
    "monthly_charges": 120.0,
    "total_charges": 7200.0,
    "contract_type": "Month-to-month",
    "payment_method": "Electronic check",
    "internet_service": "Fiber optic",
    "online_security": "No",
    "tech_support": "No",
    "num_services": 3,
    "customer_service_calls": 8
  }'
```

### Using Python
```python
import requests

url = "http://localhost:5000/predict"
data = {
    "age": 35,
    "gender": "Male",
    "tenure_months": 24,
    "monthly_charges": 75.5,
    "total_charges": 1800.0,
    "contract_type": "One year",
    "payment_method": "Credit card",
    "internet_service": "Fiber optic",
    "online_security": "Yes",
    "tech_support": "Yes",
    "num_services": 5,
    "customer_service_calls": 2
}

response = requests.post(url, json=data)
print(response.json())
```

## 📈 Model Performance

- **Best Model**: Random Forest Classifier
- **Accuracy**: ~85-90%
- **F1-Score**: ~0.85
- **ROC-AUC**: ~0.88


## 🚀 Cloud Deployment Options

### Heroku
```bash
heroku create bishsen-ml-api
git push heroku main
```

### AWS EC2
1. Launch EC2 instance
2. Install Docker
3. Deploy container

### Google Cloud Run
```bash
gcloud run deploy bishsen-ml --source .
```

## 📞 Contact

**Bishal   Mondal**  
ML Engineer | Data Scientist
contact no:9930858795
gmail:bishalmonda804@gmail.com
linkedln:www.linkedin.com/in/bishal-biplab-mondal-1b90b8399
---

## 📝 License

This project is created for educational and placement purposes.

--
