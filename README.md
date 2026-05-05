# MLR_Minor_Project

---

```markdown
🏠 House Price Prediction using Multiple Linear Regression (OOP)

📌 Project Overview
This project implements **Multiple Linear Regression (MLR)** using **Object-Oriented Programming (OOP)** concepts in Python.  
The model predicts house prices based on various features like bedrooms, bathrooms, square footage, location, and more.

---

🚀 Features
- ✅ OOP-based implementation (Class: `MLR`)
- ✅ Data preprocessing (categorical encoding)
- ✅ Train-test split
- ✅ Model training using Linear Regression
- ✅ Model evaluation (R² Score & RMSE)
- ✅ Custom prediction on new data
- ✅ Model saving & loading using Pickle
- ✅ Exception handling for robustness

---

🛠️ Technologies Used
- Python
- NumPy
- Pandas
- Scikit-learn
- Pickle

---

```
📂 Project Structure


project/

├── data.csv              # Dataset

├── model.py              # Main Python script

├── Model.pkl             # Saved trained model

├── README.md             # Project documentation

````


⚙️ How It Works

### 1. Data Loading
- Reads dataset using Pandas
- Encodes categorical columns like `city` and `country`

### 2. Data Splitting
- Splits dataset into training and testing sets (80/20)

### 3. Model Training
- Uses `LinearRegression` from Scikit-learn

### 4. Evaluation
- R² Score (Accuracy)
- RMSE (Loss)

### 5. Prediction
- Predicts house price for custom input data

### 6. Model Saving
- Saves trained model using Pickle (`Model.pkl`)
- Reloads model and verifies prediction

---

▶️ How to Run

### **Step 1: Install Dependencies**
```bash
pip install numpy pandas scikit-learn
````

### Step 2: Run the Project

```bash
python model.py
```

---

## 📊 Sample Output

```
Train Accuracy: 0.85
Train Loss: 120000.45
Test Accuracy: 0.82
Test Loss: 135000.22
Own point predictions: [450000.78]
```

---

👨‍💻 Author

**MOHAMMAD AMIR SUHAIL**

📧 Email: [amirsuhailengg01@gmail.com](mailto:amirsuhailengg01@gmail.com)

📱 Phone: 9491753326

💼 Role: Data Scientist & ML Engineer

---

📌 Future Enhancements

* 🔹 Deploy using Flask (Web App)
* 🔹 Add UI for user input
* 🔹 Use advanced models (Random Forest, XGBoost)
* 🔹 Hyperparameter tuning

---

⭐ Conclusion

This project demonstrates how **Machine Learning + OOP** can be combined to build a structured and scalable predictive model.

---

````

🚀 Real Estate Price Predictor: MLR ProjectA robust, end-to-end Machine Learning application designed to predict housing prices using Multiple Linear Regression (MLR). This project demonstrates the seamless integration of Object-Oriented Programming (OOP) for model development and a Flask web interface for real-time predictions.🛠️ Tools & Technologies UsedLanguage: Python 3.xMachine Learning: scikit-learn (Linear Regression, Model Evaluation)  Data Manipulation: pandas, numpy  Web Framework: Flask (Backend API & Routing)  Model Persistence: pickle (Saving/Loading the trained model)  Deployment: Gunicorn (WSGI HTTP Server)  Frontend: HTML/Jinja2 Templates  ⚙️ How It Works: Step-by-Step1. Data Processing & OOP ArchitectureThe core logic is encapsulated within a Python class MLR.  Initialization: Loads data.csv and performs label encoding on categorical features like 'city' and 'country' to convert them into numerical formats suitable for math.  Data Splitting: Uses an 80/20 split for training and testing to ensure the model generalizes well to unseen data.  2. Model TrainingThe model uses the LinearRegression algorithm.Training: Fits a line through the multidimensional feature space (bedrooms, sqft, floors, etc.) to minimize the error between actual and predicted prices.  Evaluation: Calculates R² Score (Accuracy) and Root Mean Squared Error (RMSE) to measure performance.  3. SerializationOnce trained, the model object reg is "pickled" into a file named Model.pkl. This allows the web server to use the model without retraining it every time.  4. Web Implementation (Flask)Backend (app.py): Loads Model.pkl. It has two main routes:/: Displays the home page.  /predict: Takes form data (user inputs), converts them to a NumPy array, and returns the predicted price to the UI.  📊 Data Insights & LogicThe model considers several critical factors from data.csv:  Internal Space: sqft_living, sqft_above, sqft_basement.Structure: bedrooms, bathrooms, floors.Location: city, country.Condition: view, waterfront, yr_built.📂 Project StructurePlaintext.
├── app.py              # Flask Backend[cite: 1]
├── main.py             # MLR Class & Training Logic[cite: 2]
├── data.csv            # Dataset[cite: 2]
├── Model.pkl           # Saved ML Model[cite: 3]
├── Procfile            # Deployment Config[cite: 4]
├── requirements.txt    # Dependencies[cite: 5]
└── templates/
    └── index.html      # Frontend UI
🚀 How to RunInstall Dependencies:Bashpip install -r requirements.txt
Train the Model:Bashpython main.py
Launch the App:Bashpython app.py
📬 Contact DetailsDeveloper: [Your Name]Email: [Your Email Address]GitHub: [Your Profile Link]LinkedIn: [Your Profile Link]
