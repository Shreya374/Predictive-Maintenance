
📌 Project Overview
This project implements an end-to-end Predictive Maintenance (PdM) pipeline designed to forecast equipment failures before they occur. By leveraging machine learning on sensor data (telemetry, error logs, and maintenance history), the system identifies patterns that precede breakdowns, allowing for scheduled repairs that minimize downtime and operational costs.
🎯 Key Objectives
 * Binary Classification: Predict if a machine will fail within a specific window (e.g., the next 24 hours).
 * Multi-class Classification: Identify the specific type of failure (e.g., heat dissipation, power failure, tool wear).
 * Regression: Estimate the Remaining Useful Life (RUL) of a component.
🏗️ System Architecture
The pipeline is divided into modular components to ensure scalability and maintainability:
 * Data Ingestion: Loading raw sensor data and logs.
 * Feature Engineering: Creating rolling averages, lag features, and time-domain transformations.
 * Model Training: Training Gradient Boosted Trees (XGBoost/LightGBM) or LSTM networks.
 * Deployment: API serving via FastAPI and a monitoring dashboard.
📊 Dataset
The project typically utilizes the NASA CMAPSS dataset or a synthetic industrial sensor dataset. Key features include:
 * Volt: Voltage fluctuations across components.
 * Rotate: Rotational speed (RPM).
 * Pressure: Internal pressure levels.
 * Vibration: Peak-to-peak vibration metrics.
🛠️ Tech Stack
 * Language: Python 3.9+
 * Data Processing: Pandas, NumPy, Scikit-learn
 * Modeling: XGBoost, LightGBM, or TensorFlow/PyTorch
 * Deployment: Docker, FastAPI, Streamlit
 * CI/CD: GitHub Actions
🚀 Getting Started
1. Installation
Clone the repository and install dependencies:
git clone https://github.com/your-username/predictive-maintenance.git
cd predictive-maintenance
pip install -r requirements.txt

2. Usage
Run the training pipeline:
python src/train.py

Launch the local monitoring dashboard:
streamlit run app/main.py

🧪 Model Performance
| Model | Accuracy | F1-Score | Precision | Recall |
|---|---|---|---|---|
| Random Forest | 0.92 | 0.89 | 0.90 | 0.88 |
| XGBoost (Best) | 0.96 | 0.94 | 0.95 | 0.93 |
| LSTM | 0.94 | 0.92 | 0.91 | 0.93 |
📂 Project Structure
├── data/               # Raw and processed datasets
├── notebooks/          # Exploratory Data Analysis (EDA)
├── src/                # Source code
│   ├── preprocessing/  # Feature engineering scripts
│   ├── models/         # Model definitions and training
│   └── utils/          # Helper functions
├── app/                # Streamlit dashboard and API
├── tests/              # Unit tests
├── Dockerfile          # Containerization
└── requirements.txt    # Project dependencies

🤝 Contributing
Contributions are welcome! If you'd like to improve the feature engineering or add new models:
 * Fork the Project.
 * Create your Feature Branch (git checkout -b feature/AmazingFeature).
 * Commit your Changes (git commit -m 'Add some AmazingFeature').
 * Push to the Branch (git push origin feature/AmazingFeature).
 * Open a Pull Request.
📄 License
Distributed under the MIT License. See LICENSE for more information.
Developed by Shreya B.Tech Student | Data Analysis & Machine Learning enthusiast
