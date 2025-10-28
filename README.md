<h1>🚗 Toyota Corolla Price Prediction using Multiple Linear Regression</h1>

<h2>📊 Project Overview</h2>
<p>This project explores the pricing dynamics of used Toyota Corolla cars using multiple linear regression techniques. The dataset contains detailed attributes of 1436 vehicles, and the goal is to build predictive models that estimate car prices based on various features.</p>

<h2>📁 Dataset Description</h2>
<ul>
  <li><strong>File:</strong> <code>ToyotaCorolla - MLR.csv</code></li>
  <li><strong>Entries:</strong> 1436 rows</li>
  <li><strong>Features:</strong> 11 columns</li>
  <li><strong>Target Variable:</strong> <code>Price</code></li>
  <li><strong>Missing Values:</strong> None</li>
</ul>

<h3>Key Features</h3>
<ul>
  <li><code>Age_08_04</code>: Age of the car in months</li>
  <li><code>KM</code>: Kilometers driven</li>
  <li><code>Fuel_Type</code>: Categorical (Petrol, Diesel, CNG)</li>
  <li><code>HP</code>: Horsepower</li>
  <li><code>Automatic</code>: Binary indicator for automatic transmission</li>
  <li><code>cc</code>: Engine capacity</li>
  <li><code>Doors</code>, <code>Cylinders</code>, <code>Gears</code>: Structural attributes</li>
  <li><code>Weight</code>: Vehicle weight</li>
</ul>

<h2>🔍 Exploratory Data Analysis (EDA)</h2>
<ul>
  <li><code>Price</code> shows a slight right-skewed distribution.</li>
  <li>Strong negative correlation with:
    <ul>
      <li><code>Age_08_04</code> (-0.88)</li>
      <li><code>KM</code> (-0.57)</li>
    </ul>
  </li>
  <li>Moderate positive correlation with:
    <ul>
      <li><code>HP</code> (0.31)</li>
      <li><code>Weight</code> (0.58)</li>
    </ul>
  </li>
  <li>Multicollinearity observed between:
    <ul>
      <li><code>Age_08_04</code> and <code>Weight</code> (0.47)</li>
      <li><code>KM</code> and <code>HP</code> (-0.33)</li>
    </ul>
  </li>
  <li>One-hot encoding applied to <code>Fuel_Type</code>.</li>
</ul>

<h2>🧠 Modeling Approach</h2>
<p>Three linear regression models were built:</p>

<table>
  <thead>
    <tr>
      <th>Model</th>
      <th>Features Used</th>
      <th>R² Score</th>
      <th>MAE</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Model 1</td>
      <td><code>Age_08_04</code>, <code>KM</code>, <code>HP</code>, <code>Weight</code>, <code>Automatic</code></td>
      <td><strong>0.8512</strong></td>
      <td>~</td>
    </tr>
    <tr>
      <td>Model 2</td>
      <td>Subset with reduced multicollinearity</td>
      <td>~</td>
      <td>~</td>
    </tr>
    <tr>
      <td>Model 3</td>
      <td>All available features</td>
      <td>0.8349</td>
      <td><strong>990.89</strong></td>
    </tr>
  </tbody>
</table>

<h3>Regularization</h3>
<ul>
  <li><strong>Lasso Regression</strong> (α = 0.1)</li>
  <li><strong>Ridge Regression</strong> (α = 1.0)</li>
  <li>Minimal impact on performance</li>
  <li>No coefficients shrunk to zero</li>
</ul>

<h2>✅ Assumptions Considered</h2>
<ul>
  <li><strong>Linearity:</strong> Assumed linear relationships; scatter plots supported this.</li>
  <li><strong>Independence of Errors:</strong> Reasonable for cross-sectional data.</li>
  <li><strong>Homoscedasticity:</strong> Assumed constant variance; residual plots not explicitly checked.</li>
  <li><strong>Normality of Errors:</strong> Slight skew in <code>Price</code> may affect inference.</li>
  <li><strong>No Perfect Multicollinearity:</strong> High correlations noted; regularization applied.</li>
</ul>

<h2>📈 Evaluation Metrics</h2>
<ul>
  <li><strong>R-squared (R²):</strong> Measures goodness of fit</li>
  <li><strong>MAE:</strong> Mean Absolute Error</li>
  <li><strong>MSE / RMSE:</strong> Mean Squared Error / Root Mean Squared Error</li>
</ul>

<h2>🛠️ Technologies Used</h2>
<ul>
  <li>Python (Pandas, NumPy, Scikit-learn)</li>
  <li>Jupyter Notebook</li>
  <li>Matplotlib / Seaborn for visualization</li>
</ul>

<h2>📚 How to Run</h2>
<ol>
  <li>Clone the repository:
    <pre><code>git clone https://github.com/your-username/toyota-corolla-price-prediction.git
cd toyota-corolla-price-prediction</code></pre>
  </li>
  <li>Install dependencies:
    <pre><code>pip install -r requirements.txt</code></pre>
  </li>
  <li>Run the notebook:
    <pre><code>jupyter notebook ToyotaCorolla_MLR_Analysis.ipynb</code></pre>
  </li>
</ol>

<h2>📌 Conclusion</h2>
<p>Model 1, with a focused feature set, provided the best predictive performance. Regularization had minimal effect with chosen hyperparameters. Future improvements could include:</p>
<ul>
  <li>Residual diagnostics</li>
  <li>Hyperparameter tuning</li>
  <li>Feature engineering</li>
</ul>

<h2>🙋‍♂️ Author</h2>
<p><strong>MARUBOTHULA</strong><br>
Aspiring Data Analyst & Full Stack Developer<br>
📍 Bengaluru, India<br>
🔗 <a href="https://www.linkedin.com/">LinkedIn</a> | <a href="https://github.com/your-username">Portfolio</a></p>
