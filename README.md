# Patient Management & Insurance Premium Predictor

This project consists of two main components: a **Patient Management System API** and an **Insurance Premium Category Predictor**. It leverages FastAPI for the backend and Streamlit for the frontend user interface.

## 🚀 Features

### 1. Patient Management System (`main.py`)
A full CRUD API to manage patient records stored in a JSON database.
- **View all patients**: Retrieve the complete list of patient records.
- **View specific patient**: Fetch details of a single patient by ID.
- **Create patient**: Add new patients with automatic BMI and health verdict calculation.
- **Update patient**: Edit existing patient details and automatically recalculate health metrics.
- **Delete patient**: Remove patient records from the system.
- **Sort patients**: Sort patients based on height, weight, or BMI in ascending or descending order.

### 2. Insurance Premium Predictor (`app.py` & `frontend.py`)
An ML-powered service that predicts the insurance premium category based on user demographics and lifestyle.
- **ML Model Integration**: Uses a pre-trained model (`model.pkl`) to predict premium categories.
- **Feature Engineering**: Automatically calculates BMI, lifestyle risk, age group, and city tier from raw input.
- **Streamlit Frontend**: A user-friendly interface for entering data and getting instant predictions.

## 🛠️ Tech Stack

- **Backend**: [FastAPI](https://fastapi.tiangolo.com/)
- **Frontend**: [Streamlit](https://streamlit.io/)
- **ML Libraries**: `scikit-learn`, `pandas`
- **Data Storage**: JSON (for patient records)
- **Server**: `uvicorn`

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd fastapi
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   # Windows
   .\venv\Scripts\activate
   # macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 🚦 Getting Started

### Running the Patient Management API
```bash
uvicorn main:app --reload
```
Access the interactive API docs at: `http://127.0.0.1:8000/docs`

### Running the Insurance Premium Predictor
1. **Start the Backend API**:
   ```bash
   uvicorn app:app --reload
   ```
2. **Start the Streamlit Frontend**:
   ```bash
   streamlit run frontend.py
   ```

## 📁 Project Structure
- `main.py`: Patient Management System API.
- `app.py`: ML Model API for Insurance Premium Prediction.
- `frontend.py`: Streamlit UI for the predictor.
- `patients.json`: JSON database for patient records.
- `model.pkl`: Pre-trained machine learning model.
- `requirements.txt`: Project dependencies.
