
# 📊 Credit Card Application Record Data Analysis & Predictive Modeling

This project provides a comprehensive analysis of application data, combining exploratory data analysis (EDA), data preprocessing, and machine learning to uncover insights and build predictive models. The goal is to understand applicant characteristics and develop a system to predict outcomes such as application approval, risk, or eligibility.

---

## 🔍 Objectives
- Explore the demographic and financial characteristics of applicants.
- Identify key patterns and relationships in the data.
- Prepare the data for machine learning by cleaning and encoding.
- Build and compare multiple classification models to predict target outcomes.
- Interpret model results to understand what drives predictions.

---

## 📁 Dataset
The project is based on a structured dataset (`application_record.csv`) with features such as:
- Applicant age, gender, income
- Family status, education, employment type
- Number of children, housing situation, etc.

---

## 📊 Exploratory Data Analysis (EDA)
EDA is performed using `Seaborn` and `Matplotlib` to visualize:
- Distribution of age, income, and family size
![alt text](image.png)

- Frequency of categorical features like gender, housing, and work type
![alt text](image-1.png)
![alt text](image-2.png)
![alt text](image-3.png)

- Correlation heatmaps to identify feature relationships
![alt text](image-6.png)
![alt text](image-7.png)

- Boxplots to detect outliers and assess variance
![alt text](image-4.png)
![alt text](image-5.png)


---

## 🧹 Data Preprocessing
- Missing values are handled appropriately (imputation or removal).
![alt text](image-8.png)
![alt text](image-9.png)
- Categorical variables are label encoded for modeling.
![alt text](image-10.png)

- The dataset is split into train and test sets for fair evaluation.
![alt text](image-11.png)

---

## 📊 Feature Importance
Important features of the model, sorting according to importance.

![alt text](image-16.png)

---

## 🤖 Machine Learning Models Peformance Before SMOTE Process
A range of classification algorithms are used to build predictive models:
- **Logistic Regression**
  ![alt text](image.png)
- **Decision Tree Classifier**
  ![alt text](image-3.png)
- **Random Forest Classifier**
  ![alt text](image-4.png)
- **XGBoost Classifier**
  ![alt text](image-7.png)
- **Extratrees Classifier**
  ![alt text](image-5.png)
- **AdaBoost Classifier**
  ![alt text](image-6.png)
- **Support Vector Machine (SVM)**
  ![alt text](image-2.png)
- **K-Nearest Neighbors (KNN)**
  ![alt text](image-1.png)

## ⚖️ SMOTE Process
Used SMOTE to balance the class distribution in the training data by generating synthetic samples for the minority class (label 1), increasing it from 893 to 5897 to match the majority class. It also scales features using StandardScaler and splits the data with train_test_split before oversampling.

## 🤖 Machine Learning Models Performance After SMOTE Process
A range of classification algorithms are used to build predictive models:
- **Logistic Regression**
  ![alt text](<images/image-26.png>)
- **Decision Tree Classifier**
  ![alt text](images/image-15.png)
- **Random Forest Classifier**
  ![alt text](images/image-22.png)
- **XGBoost Classifier**
  ![alt text](images/image-25.png)
- **Extratrees Classifier**
  ![alt text](images/image-23.png)
- **AdaBoost Classifier**
  ![alt text](images/image-24.png)
- **Support Vector Machine (SVM)**
  ![alt text](images/image-27.png)
- **K-Nearest Neighbors (KNN)**
  ![alt text](images/image-28.png)

Each model is evaluated based on its predictive performance, allowing comparison and selection of the best-performing approach.

---

## 📌 Insights & Outcomes
- Clear visualization of applicant distribution and demographic trends.
- Identification of key influencing factors via correlation and feature importance.
- Predictive modeling that can assist organizations in decision-making processes such as risk analysis or automated application approval.

## 🎯 Conclusion
Among all the models tested, Logistic Regression and K-Nearest Neighbors (KNN) delivered the most balanced performance, achieving higher F1-scores, which indicates a better trade-off between precision and recall — making them the most suitable choices for this classification task.

## 💡 Key Learning:
This project clearly demonstrates that accuracy alone is not a reliable metric in machine learning, especially when dealing with imbalanced datasets. Instead, a balanced F1-score, along with strong recall and precision for both classes, gives a more meaningful evaluation of model performance. It also highlights how class imbalance can significantly skew model results, emphasizing the importance of techniques like SMOTE to ensure fair learning.

---

## 🔗 Future Scope
- Integrate more real-world data (e.g., credit bureau reports).
- Tune hyperparameters for model optimization.
- Build a web app to deploy the prediction system.
