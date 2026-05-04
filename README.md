# MLR_Minor_Project

🚀 Real Estate Price Predictor: MLR Project
A robust, end-to-end Machine Learning application designed to predict housing prices using Multiple Linear Regression (MLR). This project demonstrates the seamless integration of Object-Oriented Programming (OOP) for model development and a Flask web interface for real-time predictions.

🛠️ Tools & Technologies Used
Language: Python 3.x

Machine Learning: scikit-learn (Linear Regression, Model Evaluation)  

Data Manipulation: pandas, numpy

  

Web Framework: Flask (Backend API & Routing)  

Model Persistence: pickle (Saving/Loading the trained model)  
+1

Deployment: Gunicorn (WSGI HTTP Server)  

Frontend: HTML/Jinja2 Templates  

⚙️ How It Works: Step-by-Step
1. Data Processing & OOP Architecture
The core logic is encapsulated within a Python class MLR.  

Initialization: Loads data.csv and performs label encoding on categorical features like 'city' and 'country' to convert them into numerical formats suitable for math.  

Data Splitting: Uses an 80/20 split for training and testing to ensure the model generalizes well to unseen data.  

2. Model Training
The model uses the LinearRegression algorithm.

Training: Fits a line through the multidimensional feature space (bedrooms, sqft, floors, etc.) to minimize the error between actual and predicted prices.  

Evaluation: Calculates R² Score (Accuracy) and Root Mean Squared Error (RMSE) to measure performance.  

3. Serialization
Once trained, the model object reg is "pickled" into a file named Model.pkl. This allows the web server to use the model without retraining it every time.  
+2

4. Web Implementation (Flask)
Backend (app.py): Loads Model.pkl. It has two main routes:

/: Displays the home page.  

/predict: Takes form data (user inputs), converts them to a NumPy array, and returns the predicted price to the UI.  

📊 Data Insights & Logic
The model considers several critical factors from data.csv:  

Internal Space: sqft_living, sqft_above, sqft_basement.

Structure: bedrooms, bathrooms, floors.

Location: city, country.

Condition: view, waterfront, yr_built.

📂 Project Structure
Plaintext
.
├── app.py              # Flask Backend[cite: 1]
├── main.py             # MLR Class & Training Logic[cite: 2]
├── data.csv            # Dataset[cite: 2]
├── Model.pkl           # Saved ML Model[cite: 3]
├── Procfile            # Deployment Config[cite: 4]
├── requirements.txt    # Dependencies[cite: 5]
└── templates/
    └── index.html      # Frontend UI
🚀 How to Run
Install Dependencies:

Bash
pip install -r requirements.txt
Train the Model:

Bash
python main.py
Launch the App:

Bash
python app.py
📬 Contact Details
Developer: [Your Name]
Email: [Your Email Address]
GitHub: [Your Profile Link]
LinkedIn: [Your Profile Link]

This project was built to demonstrate clean code practices using OOP in Machine Learning pipelines.
