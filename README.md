# ⚡ Power Plant Energy Output Predictior

## 📌 Overview

This project predicts the **Net Hourly Electrical Energy Output (PE)** of a **Combined Cycle Power Plant (CCPP)** using multiple Machine Learning and Deep Learning regression algorithms.

The project follows an end-to-end machine learning workflow, including data preprocessing, exploratory data analysis (EDA), feature scaling, model development, hyperparameter tuning, artificial neural networks, ensemble learning, model evaluation, and model persistence.

---

# 🎯 Objectives

* Predict the electrical energy output of a power plant.
* Compare the performance of multiple regression algorithms.
* Build and evaluate an Artificial Neural Network (ANN) using PyTorch.
* Implement an advanced Stacking Regressor.
* Identify the best-performing model based on R² Score.

---

# 📂 Dataset

**Combined Cycle Power Plant (CCPP) Dataset**

### Features

| Feature | Description         |
| ------- | ------------------- |
| AT      | Ambient Temperature |
| V       | Exhaust Vacuum      |
| AP      | Ambient Pressure    |
| RH      | Relative Humidity   |

### Target Variable

* **PE** — Net Hourly Electrical Energy Output

---

# 🛠️ Tech Stack

### Programming Language

* Python

### Libraries

* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* PyTorch

---

# 📊 Project Workflow

### 1. Data Preprocessing

* Loaded dataset
* Checked missing values
* Checked duplicate records
* Exploratory Data Analysis (EDA)
* Correlation analysis
* Train-Test Split
* Feature scaling using **StandardScaler**

---

### 2. Machine Learning Models

The following regression models were implemented:

* Linear Regression
* K-Nearest Neighbors (KNN) Regressor
* Support Vector Regressor (SVR)
* Decision Tree Regressor
* Random Forest Regressor
* AdaBoost Regressor
* Gradient Boosting Regressor
* Stacking Regressor

---

### 3. Deep Learning Model

An **Artificial Neural Network (ANN)** was developed using **PyTorch**.

#### ANN Architecture

* Input Layer (4 Features)
* Hidden Layer 1 — 6 Neurons + ReLU
* Hidden Layer 2 — 6 Neurons + ReLU
* Output Layer — 1 Neuron (Regression)

#### Training Configuration

* Loss Function: Mean Squared Error (MSELoss)
* Optimizer: Adam
* Batch Size: 32
* Epochs: 100
* Validation after every epoch
* Best model checkpoint saved during training

---

# ⚙️ Hyperparameter Tuning

Hyperparameter optimization was performed using **GridSearchCV** for suitable machine learning models to improve predictive performance.

Parameters tuned included:

* Number of estimators
* Maximum depth
* Learning rate
* Minimum samples split
* Number of neighbors
* Kernel parameters
* Regularization parameters

---

# 💾 Model Persistence

The best-performing Artificial Neural Network was saved using PyTorch and later reloaded for inference and evaluation.

This demonstrates how trained deep learning models can be persisted and reused without retraining.

---

# 📈 Model Performance

| Model                       | Train R² Score | Test R² Score |
| --------------------------- | -------------: | ------------: |
| ANN                         |         0.9277 |        0.9315 |
| Linear Regression           |         0.9279 |        0.9314 |
| KNN Regressor               |         0.9673 |        0.9521 |
| Support Vector Regressor    |         0.9403 |        0.9432 |
| Decision Tree Regressor     |         0.9668 |        0.9466 |
| Random Forest Regressor     |         0.9579 |        0.9520 |
| AdaBoost Regressor          |         0.9435 |        0.9425 |
| Gradient Boosting Regressor |         0.9898 |        0.9700 |
| **Stacking Regressor**      |     **0.9911** |    **0.9702** |

---

# 🏆 Best Performing Model

## **Stacking Regressor**

### Performance

* **Train R² Score:** **0.9911**
* **Test R² Score:** **0.9702**

The Stacking Regressor achieved the highest predictive performance by combining multiple strong regression models, making it the best-performing model in this project.

---

# 📁 Project Structure

```text
Power-Plant-Energy-Output-Prediction/
│
├── Dataset/
│   └── power_plant_data.csv
│
├── Notebook/
│   └── powerplant_energy_output_predictor.ipynb
│
├── Saved_Models/
│   └── best_ANN_model.pt
│
├── Output/
│   └── conclusion.txt
│
│
├── README.md
```

---

# 📌 Key Learnings

* Regression Analysis
* Data Pre-processing
* Feature Scaling
* Hyperparameter Tuning
* Ensemble Learning
* Stacking Regressor
* Artificial Neural Networks using PyTorch
* Mini-batch Gradient Descent
* Model Checkpointing
* Model Persistence
* Performance Evaluation using R² Score

---

# 🔮 Future Enhancements

* Perform feature importance analysis
* Deploy the best-performing model using Flask or FastAPI
* Build an interactive web application for predictions

---

# ⭐ If you found this project useful, consider giving the repository a star!
