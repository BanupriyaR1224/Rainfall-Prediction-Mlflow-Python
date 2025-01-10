# Rainfall Prediction Using MLflow and Python

**Project Overview**

This project aims to predict rainfall based on weather data using machine learning. The pipeline integrates data preprocessing, exploratory data analysis (EDA), model training, and deployment. The model is managed and deployed with MLflow, and a Flask web application provides a user interface for predictions.

**Features**

**Data Analysis:** Analyze and visualize weather features like pressure, humidity, and windspeed.

**Machine Learning:** Train and deploy a model to predict rainfall.

**Model Management:** Use MLflow for tracking experiments and managing the production model.

**Web Application:** Provide a user-friendly interface for inputting weather data and getting predictions.


**Project Report**

**Key Steps Observed**

**Importing Libraries:**

Libraries like pandas, numpy, matplotlib, and seaborn are used for data manipulation and visualization.

MLflow is used for tracking experiments and managing the machine learning pipeline.

**Dataset Overview:**

The dataset contains weather features such as:

pressure, maxtemp, temperature, mintemp, dewpoint, humidity, cloud, rainfall, sunshine, winddirection, and windspeed.

Example row:

pressure: 1025.9, maxtemp: 19.9, rainfall: yes, windspeed: 26.3

**Data Preprocessing:**

Steps for cleaning, feature engineering, and handling missing values are performed.

**Exploratory Data Analysis (EDA):**
     Visualizations and statistical summaries help understand the data distribution and relationships.

**Model Training:**
      A machine learning model is trained using features like pressure, humidity, and windspeed.

      Target variable: rainfall (binary classification or regression).

**MLflow Integration:**

      Experiments and model artifacts are tracked with MLflow.

      The project uses the "champion model" approach for production deployment.

**Deployment and Prediction:**

     A production-ready model is deployed using MLflow's models API.

      The notebook connects to the Flask app to provide predictions.


**Workflow**

**1.Data Preparation**

    Load and preprocess weather data from Rainfall.csv.
    
    Handle missing values and ensure data quality.
    
**2.Exploratory Data Analysis (EDA)**
    Visualize relationships between weather features.
    
    Identify patterns and trends in rainfall data.
    
**3.Model Training**
    Train a machine learning model using features such as:
    
    Pressure
    
    Dewpoint
    
    Humidity
    
    Cloud cover
    
    Sunshine
    
    Wind direction
    
    Wind speed
    
    Evaluate model performance using metrics like accuracy and recall.

**4.Model Deployment**

    Track the trained model and its metrics using MLflow.
    
    Deploy the model as a production-ready artifact.
    
**5.Web Interface**

    Use a Flask app to provide a form for entering weather data.
    
    Display predictions ("Rainfall" or "No Rainfall") dynamically based on the model's output.

**Installation**

**Prerequisites**
  Python 3.8+ ,Flask, Pandas, NumPy, Matplotlib, Seaborn, MLflow, scikit-learn

**Setup**

1.Clone this repository:

      git clone https://github.com/yourusername/rainfall-prediction.git
      
      cd rainfall-prediction
      
2.Install dependencies:

      pip install -r requirements.txt
      
3.Run the MLflow server locally:

      mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./mlruns --host 0.0.0.0 --port 5000
      
4.Start the Flask app:

      python app.py
      
5.Open your browser and go to http://127.0.0.1:8080 to use the application.

**Project Structure**
.
├── Rainfall.csv                # Dataset file

├── app.py                      # Flask application

├── index.html                  # HTML template for web UI

├── Rainfall Prediction.ipynb   # Jupyter Notebook for analysis and model training

├── requirements.txt            # Python dependencies

└── README.md                   # Project documentation

**Conclusion**

This project demonstrates the power of machine learning and data analysis for predicting rainfall using weather features. By integrating MLflow for model tracking and deploying a user-friendly Flask web application, it bridges the gap between technical model development and practical usage. With further enhancements, this project can serve as a robust foundation for real-world weather prediction systems.
