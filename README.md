🚰 Smart Pipeline Leak Detection System using Machine Learning


📌 Overview

This project presents a machine learning-based solution for detecting pipeline leaks and predicting their location (distance) and severity (diameter) using sensor data.

Traditional leak detection methods are often manual, time-consuming, and hardware-intensive. This system leverages pressure and flow sensor readings to automatically identify leaks, improving efficiency and reducing water loss.

🎯 Objectives

Detect pipeline leaks using sensor data
Predict leak distance from the pipeline inlet
Estimate leak size (diameter/burst size)
Improve reliability of pipeline monitoring systems

🧠 Problem Statement

Pipeline leaks lead to:

Water/resource wastage
Financial losses
Delayed maintenance

The goal is to build a data-driven ML system that can:

Automatically detect leaks
Provide actionable insights for faster response

📊 Dataset Description

The dataset is based on an experimental pipeline setup and contains multiple leak scenarios.

🔹 Features (Input)
P1 – Inlet Pressure
P2 – Outlet Pressure
Q1 – Inlet Flow Rate
Q2 – Outlet Flow Rate
🔹 Targets (Output)
Leak Distance (continuous value)
Leak Diameter (continuous value)
🔹 Dataset Characteristics
Multiple experimental leak scenarios
Includes variations in:
Leak positions
Leak sizes
Stored in NumPy (.npy) files
⚙️ Tech Stack
🐍 Programming Language
Python
📦 Libraries & Tools
NumPy – numerical computations and array handling
Pandas – data manipulation and preprocessing
Scikit-learn – ML models, preprocessing, evaluation
XGBoost – advanced boosting algorithm
Matplotlib – data visualization
Joblib – model saving and loading
🔄 Machine Learning Pipeline
1️⃣ Data Preprocessing
Merged multiple .npy files into a unified dataset
Handled missing values and noisy sensor readings
Removed outliers caused by sensor fluctuations
Standardized features for better model performance
Split data into training (70%) and testing (30%)
2️⃣ Models Implemented

We experimented with multiple ML algorithms:

K-Nearest Neighbors (KNN)
Decision Tree
Random Forest
Support Vector Machine (SVM)
XGBoost
3️⃣ Final Model Selection
✅ Random Forest → Best for Leak Diameter Prediction
✅ XGBoost → Best for Leak Distance Prediction
Why?
Random Forest handles noisy sensor data effectively
XGBoost captures fine-grained patterns in pressure/flow changes

Both are ensemble models, improving accuracy and stability.

📈 Evaluation Metrics

We evaluated models using:

RMSE (Root Mean Squared Error) → Penalizes large errors
MAE (Mean Absolute Error) → Average prediction error
R² Score → Model’s ability to explain data variation

🚀 Results

Achieved 85%+ prediction accuracy
Improved reliability of leak detection
Successfully predicted:
Leak location
Leak severity

🌍 Applications

Water distribution systems
Oil & gas pipelines
Industrial fluid transport systems
Smart infrastructure monitoring

⚠️ Challenges Faced

Handling noisy and nonlinear sensor data
Poor performance of simple models initially
Required model tuning and ensemble techniques

🔮 Future Improvements

Integrate real-time IoT sensor data
Deploy as a web-based monitoring dashboard
Use deep learning for time-series analysis
Expand dataset for more real-world scenarios

How to Run
1. Clone the repository
git clone https://github.com/your-username/pipeline-leak-detection.git
cd pipeline-leak-detection
2. Install dependencies
pip install -r requirements.txt
3. Run the model
python train.py

📄 Publication

This work has been published in IEEE, demonstrating its practical relevance and research contribution.
[LINK](https://ieeexplore.ieee.org/document/10625634)

⭐ Acknowledgements

Experimental dataset contributors
Open-source ML libraries


💡 Final Note

This project demonstrates how machine learning + sensor data can solve real-world infrastructure problems by improving efficiency, reducing losses, and enabling smarter monitoring systems.
Deploy as a web-based monitoring dashboard
Use deep learning for time-series analysis
Expand dataset for more real-world scenarios
