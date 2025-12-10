📌 Overview
This project is an end-to-end Machine Learning pipeline designed to predict the onset of diabetes using the **Pima Indians Diabetes Dataset**. The workflow includes comprehensive data preprocessing, exploratory data analysis (EDA), and the comparative evaluation of five different classification algorithms to identify the best model for early diagnosis.

📂 Dataset
Source: Pima Indians Diabetes Dataset
Description: Diagnostic measurements (e.g., Glucose, BMI, Insulin, Age) for female patients at least 21 years old of Pima Indian heritage.
Target: `Outcome` (0 = Non-Diabetic, 1 = Diabetic)

🛠️ Technologies Used
Language**: Python
Libraries**:
    * `pandas` & `numpy` (Data Manipulation)
    * `matplotlib` & `seaborn` (Visualization)
    * `scikit-learn` (Machine Learning & Preprocessing)

Project Workflow
1. Data Preprocessing
* Data Cleaning: Replaced zeros (missing values) in `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI` with the column **median**.
* Encoding: Applied Label Encoding to the target variable.
* Scaling: Normalized features using `StandardScaler` to optimize model convergence.
* Splitting: Divided data into **80% Training** and **20% Testing** sets.

2. Exploratory Data Analysis (EDA)
* Histograms: To visualize feature distributions.
* Correlation Heatmap: To identify relationships between diagnostic features (e.g., Glucose vs. Outcome).
* Scatter Plots: To observe clusters between diabetic and non-diabetic patients.
 3. Model Training
Five classification algorithms were trained and tested:
1.  Logistic Regression
2.  K-Nearest Neighbors (KNN)
3.  Decision Tree Classifier
4.  Random Forest Classifier
5.  Support Vector Machine (SVM)

📊 Results & Evaluation
Models were evaluated using **Accuracy**, **Precision**, **Recall**, **F1-Score**, and **ROC-AUC**.

| Model | Accuracy | F1-Score | ROC AUC |
| :--- | :--- | :--- | :--- |
| **Logistic Regression** | 75.3% | 0.64 | 0.82 |
| **KNN** | 73.4% | 0.65 | 0.77 |
| **Decision Tree** | 71.4% | 0.61 | 0.69 |
| **Random Forest** | **74.0%** | **0.64** | **0.83** |
| **SVM** | 74.7% | 0.62 | 0.81 |

Best Performer: The **Random Forest Classifier** achieved the highest ROC-AUC score (0.83), indicating superior capability in distinguishing between classes.

📈 Visualizations
The project generates the following plots:
* `confusion_matrices.png`: Detailed error analysis for each model.
* `roc_curves.png`: Performance comparison of True Positive Rate vs. False Positive Rate.
* `learning_curves.png`: Analysis of overfitting vs. underfitting.
