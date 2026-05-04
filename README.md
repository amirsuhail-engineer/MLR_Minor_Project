# MLR_Minor_Project

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MLR Project Documentation</title>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.6; color: #333; max-width: 900px; margin: auto; padding: 20px; background-color: #f4f7f6; }
        header { background: #2c3e50; color: white; padding: 2rem; text-align: center; border-radius: 8px; margin-bottom: 20px; }
        .container { background: white; padding: 30px; border-radius: 8px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
        h2 { color: #2c3e50; border-bottom: 2px solid #3498db; padding-bottom: 10px; margin-top: 30px; }
        .tool-tag { display: inline-block; background: #e1f5fe; color: #0277bd; padding: 5px 12px; border-radius: 15px; font-size: 0.9em; margin: 5px; font-weight: bold; }
        code { background: #f8f8f8; border: 1px solid #ddd; padding: 2px 5px; border-radius: 4px; font-family: 'Courier New', Courier, monospace; }
        .step-box { border-left: 4px solid #3498db; padding-left: 15px; margin: 20px 0; }
        .highlight { color: #e67e22; font-weight: bold; }
        table { width: 100%; border-collapse: collapse; margin: 20px 0; }
        th, td { text-align: left; padding: 12px; border-bottom: 1px solid #ddd; }
        th { background-color: #3498db; color: white; }
    </style>
</head>
<body>

<header>
    <h1>Multiple Linear Regression (MLR) Project</h1>
    <p>End-to-End Real Estate Price Prediction using OOP & Flask</p>
</header>

<div class="container">
    <h2>🛠️ Tools & Technologies</h2>
    <div>
        <span class="tool-tag">Python 3.x</span>
        <span class="tool-tag">Flask (Web Framework)</span>
        <span class="tool-tag">Pandas (Data Manipulation)</span>
        <span class="tool-tag">NumPy (Numerical Computing)</span>
        <span class="tool-tag">Scikit-Learn (ML Algorithms)</span>
        <span class="tool-tag">Pickle (Model Serialization)</span>
        <span class="tool-tag">Gunicorn (WSGI HTTP Server)</span>
    </div>

    <h2>📊 Project Architecture</h2>
    <p>The project is divided into two primary phases: <strong>Model Development</strong> using OOP principles and <strong>Web Deployment</strong> via a Flask backend.</p>
    
    

    <h2>🚀 Step-by-Step Implementation</h2>

    <div class="step-box">
        <h3>Step 1: Data Preprocessing & Class Initialization</h3>
        <p>The <code>MLR</code> class is initialized with the <code>data.csv</code> file. The code performs <strong>Label Encoding</strong> manually on categorical features like <code>city</code> and <code>country</code> to convert them into numerical formats suitable for the regression model[cite: 2].</p>
    </div>

    <div class="step-box">
        <h3>Step 2: Model Training</h3>
        <p>Using <code>sklearn.linear_model.LinearRegression</code>, the model learns the relationship between independent variables (bedrooms, sqft, built year, etc.) and the target variable (price)[cite: 2].</p>
        
    </div>

    <div class="step-box">
        <h3>Step 3: Performance Evaluation</h3>
        <p>The model's accuracy is measured using <code>r2_score</code> and <code>root_mean_squared_error</code>. This ensures the model generalizes well to unseen testing data[cite: 2].</p>
    </div>

    <div class="step-box">
        <h3>Step 4: Serialization (Model Persistence)</h3>
        <p>The trained model object <code>m</code> is saved as <code>Model.pkl</code> using the <strong>Pickle</strong> library. This allows the Flask backend to load the "brain" of the project without retraining[cite: 1, 2].</p>
    </div>

    <div class="step-box">
        <h3>Step 5: Web Integration (Flask)</h3>
        <p>The <code>app.py</code> file creates two routes:
            <ul>
                <li><code>/</code>: Renders the <code>index.html</code> landing page[cite: 1].</li>
                <li><code>/predict</code>: Collects form data, converts it to a NumPy array, and uses <code>m.predict()</code> to return the estimated price[cite: 1].</li>
            </ul>
        </p>
    </div>

    <h2>📈 Feature Breakdown</h2>
    <table>
        <thead>
            <tr>
                <th>Feature Category</th>
                <th>Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><strong>Structural</strong></td>
                <td>Bedrooms, Bathrooms, Floors, Sqft Living/Lot</td>
            </tr>
            <tr>
                <td><strong>Condition</strong></td>
                <td>Waterfront, View, Overall Condition</td>
            </tr>
            <tr>
                <td><strong>Temporal</strong></td>
                <td>Year Built, Year Renovated</td>
            </tr>
            <tr>
                <td><strong>Location</strong></td>
                <td>City, Country (USA)</td>
            </tr>
        </tbody>
    </table>

    <h2>⚙️ How to Run</h2>
    <ol>
        <li>Ensure <code>data.csv</code> and <code>Model.pkl</code> are in the root directory.</li>
        <li>Install dependencies: <code>pip install -r requirements.txt</code>[cite: 5].</li>
        <li>Run the trainer script to generate/update the model: <code>python train_script.py</code>.</li>
        <li>Start the web server: <code>python app.py</code> or use <code>gunicorn app:app</code> for production[cite: 1, 4].</li>
    </ol>

    <p style="text-align: center; margin-top: 50px; color: #7f8c8d;">
        <i>Created with a focus on clean code and Object-Oriented Design.</i>
    </p>
</div>

</body>
</html>
