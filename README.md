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

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <style>
        @page {
            size: A4;
            margin: 15mm;
            background-color: #f8fafc;
        }
        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            line-height: 1.6;
            color: #1e293b;
            margin: 0;
            padding: 0;
        }
        .container {
            background: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1);
        }
        .header {
            background: #1e40af;
            color: white;
            padding: 40px;
            text-align: center;
            border-radius: 8px 8px 0 0;
            margin: -30px -30px 30px -30px;
        }
        h1 { margin: 0; font-size: 24pt; }
        h2 { 
            color: #1e40af; 
            border-bottom: 2px solid #e2e8f0; 
            padding-bottom: 8px; 
            margin-top: 30px;
            font-size: 16pt;
        }
        h3 { color: #334155; font-size: 13pt; margin-top: 20px; }
        .tag {
            display: inline-block;
            background: #dbeafe;
            color: #1e40af;
            padding: 4px 12px;
            border-radius: 15px;
            font-size: 9pt;
            font-weight: bold;
            margin: 4px;
        }
        .file-box {
            background: #f1f5f9;
            border-left: 4px solid #3b82f6;
            padding: 12px;
            margin: 10px 0;
            font-family: monospace;
            font-size: 10pt;
        }
        .step-card {
            border: 1px solid #e2e8f0;
            padding: 15px;
            margin: 15px 0;
            border-radius: 8px;
        }
        .math {
            font-family: 'Times New Roman', serif;
            font-style: italic;
            font-weight: bold;
            color: #1e40af;
        }
        .visual-box {
            background: #f8fafc;
            border: 2px dashed #cbd5e1;
            padding: 20px;
            text-align: center;
            color: #64748b;
            margin: 15px 0;
            border-radius: 8px;
        }
        .footer {
            margin-top: 40px;
            padding: 20px;
            border-top: 2px solid #e2e8f0;
            background: #f8fafc;
        }
        table { width: 100%; border-collapse: collapse; margin: 15px 0; }
        th, td { text-align: left; padding: 12px; border-bottom: 1px solid #e2e8f0; }
        th { background: #f8fafc; }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>House Price Prediction Engine</h1>
            <p>End-to-End Machine Learning Web Application</p>
        </div>

        <section>
            <h2>🚀 Project Overview</h2>
            <p>This project leverages <strong>Multiple Linear Regression (MLR)</strong> to predict real estate prices based on 13 distinct features. Built with a modular Object-Oriented Programming (OOP) approach, it bridges the gap between raw data science and a functional web interface.</p>
            <div>
                <span class="tag">Python</span> <span class="tag">Flask</span> <span class="tag">Scikit-Learn</span> 
                <span class="tag">Pandas</span> <span class="tag">NumPy</span> <span class="tag">Gunicorn</span>
            </div>
        </section>

        <section>
            <h2>🛠️ Tools & Technologies</h2>
            <table>
                <tr><th>Category</th><th>Tools Used</th></tr>
                <tr><td><strong>Core Logic</strong></td><td>Python (OOP Architecture)</td></tr>
                <tr><td><strong>Data Processing</strong></td><td>Pandas, NumPy</td></tr>
                <tr><td><strong>ML Modeling</strong></td><td>Scikit-Learn (LinearRegression)</td></tr>
                <tr><td><strong>Web Framework</strong></td><td>Flask, Jinja2 Template Engine</td></tr>
                <tr><td><strong>Deployment</strong></td><td>Gunicorn (WSGI), Render Platform</td></tr>
            </table>
        </section>

        <section>
            <h2>📝 File Architecture</h2>
            <div class="file-box"><strong>main.py:</strong> The ML Engine. Handles Data Cleaning, Mapping, and Model Training.</div>
            <div class="file-box"><strong>app.py:</strong> The Web Server. Connects the model to the HTML frontend.</div>
            <div class="file-box"><strong>Model.pkl:</strong> The brain. A serialized file containing the trained weights.</div>
            <div class="file-box"><strong>data.csv:</strong> The dataset (House prices in Seattle/USA).</div>
            <div class="file-box"><strong>requirements.txt:</strong> List of all Python dependencies.</div>
        </section>

        <section>
            <h2>⚙️ The Workflow: Step-by-Step</h2>

            <div class="step-card">
                <h3>Step 1: Data Pre-processing</h3>
                <p>The <code>MLR</code> class in <code>main.py</code> reads the CSV and performs encoding. Categorical data like <em>City</em> and <em>Country</em> are mapped to numerical values because ML algorithms only understand numbers.</p>
                <div class="visual-box">
                    <strong>[Graph: Feature Correlation Heatmap]</strong><br>
                    Shows how features like 'sqft_living' correlate strongly with 'price'.
                </div>
            </div>

            <div class="step-card">
                <h3>Step 2: Training the Algorithm</h3>
                <p>We split the data into <strong>80% Training</strong> and <strong>20% Testing</strong>. The model learns the relationship:</p>
                <div style="text-align:center; margin:1em 0; font-size:1.1em;">
                    <span class="math">Price = β₀ + β₁x₁ + β₂x₂ + ... + βₙxₙ + ε</span>
                </div>
                <div class="visual-box">
                    <strong>[Image: Linear Regression Fit Line]</strong><br>
                    Illustrating the best-fit line through a scatter plot of data points.
                </div>
            </div>

            <div class="step-card">
                <h3>Step 3: Serialization</h3>
                <p>Using <code>pickle</code>, we "freeze" the trained model into <code>Model.pkl</code>. This ensures we don't need to retrain the model every time a user visits the website.</p>
            </div>

            <div class="step-card">
                <h3>Step 4: Web Deployment</h3>
                <p><code>app.py</code> initializes a Flask server. It captures user inputs from the web form, feeds them into the <code>.pkl</code> file, and displays the predicted price instantly.</p>
            </div>
        </section>

        <div class="footer">
            <h2>👤 Contact Information</h2>
            <p><strong>Name:</strong> Mohammad Amir Suhail</p>
            <p><strong>Role:</strong> Data Science Professional & Student</p>
            <p><strong>Institution:</strong> Jawaharlal Nehru Technological University Hyderabad</p>
            <p><strong>Project Link:</strong> Simple_LinearRegression_Project</p>
        </div>
    </div>
</body>
</html>

Specialization: Data Science & Data Analysis  
