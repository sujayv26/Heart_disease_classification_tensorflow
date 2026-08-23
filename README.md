````markdown
# Heart_disease_classification_tensorflow

MLOPS Assignment

# ❤️ Heart Disease Classification using TensorFlow

## 📌 Project Overview

This project implements a **Neural Network Classification model using TensorFlow and Keras** to predict **heart disease** based on different patient-related features.

The project demonstrates the complete machine learning workflow, including data preprocessing, feature scaling, model development, training, evaluation, ensemble prediction, and visualization using Python.

Three different neural network models are trained independently, and their prediction probabilities are combined using an **averaging ensemble technique**.

---

## 🎯 Objective

To build a TensorFlow-based classification model capable of predicting the presence or absence of heart disease using various patient-related features.

The project also demonstrates how multiple neural network models can be combined using an ensemble technique to generate a final prediction.

---

## 📂 Dataset

**Dataset Name:** Heart Disease UCI Dataset

The dataset contains **303 records** with **13 input features**.

### Features

- Age
- Sex
- Chest Pain Type
- Resting Blood Pressure
- Serum Cholesterol
- Fasting Blood Sugar
- Resting ECG Results
- Maximum Heart Rate Achieved
- Exercise-Induced Angina
- ST Depression
- Slope of Peak Exercise ST Segment
- Number of Major Vessels
- Thalassemia

### Target Variable

The target variable represents the presence or absence of heart disease.

- **0 – No Disease**
- **1 – Disease**

Since the target variable contains two classes, this is a **binary classification problem**.

### Dataset Details

- Total Records: **303**
- Total Input Features: **13**
- Training Data: **80%**
- Testing Data: **20%**
- Target Classes: **2**
- Feature Scaling: **StandardScaler**
- Missing Values: **Checked using Pandas**

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow
- Keras
- Jupyter Notebook

---

## 📁 Project Structure

```text
Heart_disease_classification_tensorflow/
│
├── heart.csv
├── heart_disease_classification.ipynb
├── README.md
└── Report/
    └── Experiment_4_Report.pdf
````

---

## ⚙️ Workflow

1. Import required libraries
2. Load the dataset
3. Explore the dataset
4. Check dataset shape and columns
5. Check dataset information
6. Display statistical summary
7. Check for missing values
8. Analyze target distribution
9. Select input features and target variable
10. Split the dataset into training and testing sets
11. Scale input features using StandardScaler
12. Build the TensorFlow Keras neural network
13. Define three different neural network models
14. Train the models
15. Evaluate individual models
16. Generate prediction probabilities
17. Combine model predictions using averaging ensemble
18. Calculate ensemble accuracy
19. Compare individual and ensemble model accuracies
20. Generate confusion matrix
21. Generate classification report
22. Analyze model performance

---

## 🧠 Model Architecture

The classification models were developed using **TensorFlow and Keras**.

### Neural Network Structure

```text
Input Layer
     ↓
Dense Layer – Variable Neurons
     ↓
Dense Layer – Variable Neurons
     ↓
Output Layer – 1 Neuron
```

The hidden layers use the **ReLU activation function**, while the output layer uses the **Sigmoid activation function** for binary classification.

### Model Configuration

| Model   | First Hidden Layer | Second Hidden Layer | Random Seed |
| ------- | ------------------ | ------------------- | ----------- |
| Model 1 | 16 Neurons         | 8 Neurons           | 1           |
| Model 2 | 32 Neurons         | 16 Neurons          | 2           |
| Model 3 | 8 Neurons          | 8 Neurons           | 3           |

### Training Configuration

* Optimizer: **Adam**
* Loss Function: **Binary Cross-Entropy**
* Evaluation Metric: **Accuracy**
* Hidden Layer Activation: **ReLU**
* Output Activation: **Sigmoid**
* Epochs: **50**
* Batch Size: **16**

---

## 🤝 Ensemble Technique

Three different neural network models were trained independently using the training dataset.

Each model generates a probability prediction for every test sample.

The prediction probabilities from all three models are combined using an averaging ensemble technique.

### Ensemble Formula

```text
Ensemble Probability =
(Model 1 Probability +
 Model 2 Probability +
 Model 3 Probability) / 3
```

The final class is determined using a threshold of **0.5**.

```text
Probability > 0.5  → Disease (1)

Probability ≤ 0.5 → No Disease (0)
```

---

## 📊 Model Evaluation

The trained models were evaluated using standard classification metrics such as **Accuracy, Precision, Recall, F1-Score, and Confusion Matrix**.

### Model Accuracy

| Model              | Accuracy   |
| ------------------ | ---------- |
| Model 1            | **80.33%** |
| Model 2            | **78.69%** |
| Model 3            | **81.97%** |
| Ensemble (Average) | **80.33%** |

The best individual model was **Model 3**, which achieved an accuracy of **81.97%**.

The averaging ensemble achieved an accuracy of **80.33%**.

---

## 📉 Confusion Matrix

The ensemble model produced the following confusion matrix:

```text
[[20  8]
 [ 4 29]]
```

### Confusion Matrix Details

* **20** – True Negatives
* **8** – False Positives
* **4** – False Negatives
* **29** – True Positives

The ensemble model correctly classified **20 patients without heart disease** and **29 patients with heart disease**.

It incorrectly classified **8 patients without heart disease as having disease** and **4 patients with heart disease as having no disease**.

---

## 📋 Classification Report

### No Disease Class

* Precision: **0.83**
* Recall: **0.71**
* F1-Score: **0.77**
* Support: **28**

### Disease Class

* Precision: **0.78**
* Recall: **0.88**
* F1-Score: **0.83**
* Support: **33**

### Overall Performance

* Accuracy: **0.80**
* Macro Average F1-Score: **0.80**
* Weighted Average F1-Score: **0.80**

The disease class achieved a recall of **0.88**, indicating that the model correctly identified a large proportion of patients belonging to the disease class.

---

## 📈 Visualizations

The project includes:

* Target Distribution Plot
* Model Accuracy Comparison
* Confusion Matrix
* Classification Performance Analysis

These visualizations help analyze the dataset distribution and compare the performance of the individual neural network models and the ensemble model.

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/sujayv26/Heart_disease_classification_tensorflow.git
```

### 2. Navigate to the Project

```bash
cd Heart_disease_classification_tensorflow
```

### 3. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter
```

### 4. Run the Notebook

```bash
jupyter notebook
```

Open **heart_disease_classification.ipynb** and execute all cells.

---

## 📦 Required Libraries

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
tensorflow
jupyter
```

---

## 📌 Results

* Successfully developed a **TensorFlow-based neural network classification model**.
* Successfully classified patients into **No Disease** and **Disease** classes.
* Developed and trained **three different neural network models**.
* Model 1 achieved an accuracy of **80.33%**.
* Model 2 achieved an accuracy of **78.69%**.
* Model 3 achieved the highest individual accuracy of **81.97%**.
* The averaging ensemble achieved an accuracy of **80.33%**.
* The ensemble model achieved an F1-Score of **0.77** for the No Disease class.
* The ensemble model achieved an F1-Score of **0.83** for the Disease class.
* The ensemble model achieved a recall of **0.88** for the Disease class.
* Successfully demonstrated an end-to-end binary classification workflow using TensorFlow and Keras.
* Successfully demonstrated ensemble learning by combining predictions from multiple neural networks.

---

## 📚 Learning Outcomes

* Data Loading and Exploration
* Data Preprocessing
* Missing Value Analysis
* Feature Scaling
* Train-Test Splitting
* TensorFlow and Keras
* Neural Network Classification
* Binary Classification
* Model Training
* Ensemble Learning
* Prediction Probability Averaging
* Model Evaluation
* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Data Visualization
* GitHub Project Management

---

## 👨‍💻 Author

**Sujay V**

B.Tech CSE (AI Driven DevOps)

Jain University

---

## 📄 License

This project was developed for educational purposes as part of a **Machine Learning Operations laboratory assignment**.

```
```
