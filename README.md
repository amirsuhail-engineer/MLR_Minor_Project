# MLR_Minor_Project

import pandas as pd

# Load the data to get column names and some statistics for the README
try:
    df = pd.read_csv('data.csv')
    columns = df.columns.tolist()
    shape = df.shape
except Exception:
    columns = ["price", "bedrooms", "sqft_living", "city"]
    shape = (4600, 15)

readme_content = f"""# 🏠 Real Estate Price Predictor

A complete End-to-End Machine Learning application built using **Multiple Linear Regression (MLR)**, Object-Oriented Programming (OOP), and Flask. This project predicts house prices based on various features like square footage, location, and property condition.

---

## 🛠 Tools & Technologies

The project leverages a modern data science and web stack:

* **Language:** ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) - The core logic and model training.
* **Data Manipulation:** ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) - Used for cleaning and processing the house data.
* **Machine Learning:** ![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) - Powers the Multiple Linear Regression model.
* **Web Framework:** ![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white) - Serves the predictive model through a web interface.
* **Deployment:** ![Gunicorn](https://img.shields.io/badge/gunicorn-%23499848.svg?style=for-the-badge&logo=gunicorn&logoColor=white) - WSGI HTTP Server for production deployment.

---

## 📊 Dataset Overview

The model is trained on a dataset containing property listings with features like:

| Feature | Description |
| :--- | :--- |
| **sqft_living** | Square footage of the interior living space |
| **bedrooms/bathrooms** | Count of rooms available in the property |
| **city** | Location (Categorical, mapped to integers for the model) |
| **condition** | Overall condition rating (1 to 5) |
| **yr_built** | The year the property was originally constructed |

---

## 🚀 Step-by-Step Implementation

### 1. The Blueprint (`main.py`)
This file uses **Object-Oriented Programming (OOP)** to ensure the code is modular and reusable.
* **Data Ingestion**: The `MLR` class loads `data.csv`.
* **Preprocessing**: It maps text-based cities to numbers and handles feature selection (`X` and `y`).
* **Training**: Splits the data (80/20) and trains the `LinearRegression` model.
* **Serialization**: Saves the brain of the app as `Model.pkl`.

### 2. The Brain (`Model.pkl`)
This is a serialized file containing the mathematical weights and biases calculated during training. It allows the app to make instant predictions without retraining.

### 3. The Engine (`app.py`)
A Flask server that:
* Renders the `index.html` frontend.
* Accepts form data via `POST` requests.
* Feeds the data into the loaded model and displays the result.

### 4. Production Ready (`Procfile` & `requirements.txt`)
* `requirements.txt` ensures all libraries (like `scikit-learn==1.8.0`) are consistent.
* `Procfile` defines the entry point for cloud hosting platforms.

---

## ⚙️ How It Works (Visual Flow)

### Mathematical Logic
The model follows the Multiple Linear Regression formula:
**$Y = \beta_0 + \beta_1X_1 + \beta_2X_2 + ... + \beta_nX_n$**

Where:
* $Y$ is the Predicted Price.
* $X$ are the house features (sqft, bedrooms, etc.).
* $\beta$ are the coefficients learned during training.

### Data Workflow
1.  **Input**: User enters house details on the web form.
2.  **Process**: Flask parses inputs into a NumPy array.
3.  **Inference**: The model calculates the dot product of inputs and learned coefficients.
4.  **Output**: The estimated price is displayed on the screen.

---

## 🛠 Setup Instructions

1. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
