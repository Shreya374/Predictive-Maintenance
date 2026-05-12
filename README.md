# 🔧 Predictive Maintenance — End-to-End ML Pipeline

> **Forecast equipment failures before they occur — minimise downtime, reduce costs, and extend asset life using machine learning on sensor data.**

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-Best%20Model-red?style=for-the-badge)
![FastAPI](https://img.shields.io/badge/FastAPI-Deployment-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

## 📌 Project Overview

This project implements an **end-to-end Predictive Maintenance (PdM) pipeline** designed to forecast equipment failures before they occur. By leveraging machine learning on sensor data — telemetry, error logs, and maintenance history — the system identifies patterns that precede breakdowns, enabling scheduled repairs that minimise downtime and operational costs.

![Predictive Maintenance Pipeline](https://www.intellisoft.io/wp-content/uploads/2023/06/iot-predictive-maintenance-intellisoft.jpg)
*From raw sensor data to actionable failure predictions*

---

## 🎯 Key Objectives

| Task | Description |
|------|-------------|
| 🔴 **Binary Classification** | Predict if a machine will fail within a specific window (e.g., next 24 hours) |
| 🟠 **Multi-class Classification** | Identify the specific failure type (heat dissipation, power failure, tool wear) |
| 📉 **Regression (RUL)** | Estimate the **Remaining Useful Life** of a component |

---

## 🏗️ System Architecture

The pipeline is divided into **modular components** to ensure scalability and maintainability:

```
┌─────────────────────────────────────────────────────────────────┐
│                  PREDICTIVE MAINTENANCE PIPELINE                │
└─────────────────────────────────────────────────────────────────┘

  📥 Data Ingestion        Raw sensor data, telemetry, error logs
         │
         ▼
  🔧 Feature Engineering   Rolling averages, lag features, time-domain transforms
         │
         ▼
  🤖 Model Training        XGBoost / LightGBM / LSTM networks
         │
         ▼
  📊 Evaluation            Accuracy, F1-Score, ROC-AUC, Confusion Matrix
         │
         ▼
  🚀 Deployment            FastAPI REST endpoint + Streamlit dashboard
```

---

## 📊 Dataset

The project uses the **NASA CMAPSS dataset** or a synthetic industrial sensor dataset.

| Feature | Description |
|---------|-------------|
| ⚡ `Volt` | Voltage fluctuations across components |
| 🔄 `Rotate` | Rotational speed (RPM) |
| 💨 `Pressure` | Internal pressure levels |
| 📳 `Vibration` | Peak-to-peak vibration metrics |

---

## 🛠️ Tech Stack

| Layer | Tools |
|-------|-------|
| **Language** | Python 3.9+ |
| **Data Processing** | Pandas, NumPy, Scikit-learn |
| **Modeling** | XGBoost, LightGBM, TensorFlow / PyTorch |
| **Deployment** | Docker, FastAPI, Streamlit |
| **CI/CD** | GitHub Actions |

---

## 🚀 Getting Started

### Installation

```bash
# Clone the repository
git clone https://github.com/Shreya374/Predictive-Maintenance.git
cd Predictive-Maintenance

# Install dependencies
pip install -r requirements.txt
```

### Usage

```bash
# Run the training pipeline
python src/train.py

# Launch the local monitoring dashboard
streamlit run app/main.py
```

---

## 🧪 Model Performance

| Model | Accuracy | F1-Score | Precision | Recall |
|-------|----------|----------|-----------|--------|
| Random Forest | 0.92 | 0.89 | 0.90 | 0.88 |
| ⭐ **XGBoost (Best)** | **0.96** | **0.94** | **0.95** | **0.93** |
| LSTM | 0.94 | 0.92 | 0.91 | 0.93 |

> 🏆 **XGBoost** achieved the best overall performance with **96% accuracy** and **0.94 F1-Score**.

---

## 📂 Project Structure

```
Predictive-Maintenance/
│
├── 📁 data/                  # Raw and processed datasets
├── 📓 notebooks/             # Exploratory Data Analysis (EDA)
├── 📁 src/                   # Source code
│   ├── preprocessing/        # Feature engineering scripts
│   ├── models/               # Model definitions and training
│   └── utils/                # Helper functions
├── 📁 app/                   # Streamlit dashboard and FastAPI
├── 📁 tests/                 # Unit tests
├── 🐳 Dockerfile             # Containerization
└── 📄 requirements.txt       # Project dependencies
```

---

## 🤝 Contributing

Contributions are welcome! If you'd like to improve the feature engineering or add new models:

1. **Fork** the project
2. **Create** your feature branch
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit** your changes
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push** to the branch
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open** a Pull Request

---

## 📄 License

Distributed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🤓 About Me

B.Tech Computer Science graduate and **Data Analyst intern** with hands-on experience in Python, SQL, machine learning, and end-to-end data pipelines. Passionate about applying ML to solve real-world industrial and business problems.

[![GitHub](https://img.shields.io/badge/GitHub-Shreya374-181717?style=flat-square&logo=github)](https://github.com/Shreya374)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-shreya--jagtap-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/shreya-jagtap)
[![Email](https://img.shields.io/badge/Email-shreyajagtap374@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:shreyajagtap374@gmail.com)

---

⭐ *If you found this project helpful, consider starring the repository!*
