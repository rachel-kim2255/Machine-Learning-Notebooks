# Machine-Learning-Notebooks
Documenting my journey through Machine Learning. This repository features step-by-step implementations of various models, from Linear Regression to Advanced Boosting techniques.

---

## 1. [Linear Model] Predicting Insurance Premiums 

[![Jupyter Notebook](https://img.shields.io/badge/Notebook-View%20on%20GitHub-orange?logo=jupyter&logoColor=white)](https://github.com/rachel-kim2255/Machine-Learning-Notebooks/blob/main/1_%5BML_Linear_Model%5D_Predicting_Insurance_Premiums.ipynb)

> This project aims to forecast insurance costs by leveraging demographic and health indicators, such as **age, gender, and BMI**. The primary goal is to understand the practical application of **linear regression** and interpret how individual features influence medical charges.

### **Key Results**
* **R² Score**: 0.736 (Explains ~73.6% of the variance)
* **RMSE**: 5,684
* **Main Insight**: Smoking status and age were identified as the most significant predictors of insurance premiums.

*[2026-Jan]*

---

## 2. [Logistic Regression] Titanic Survival Prediction
[![Jupyter Notebook](https://img.shields.io/badge/Notebook-View%20on%20GitHub-orange?logo=jupyter&logoColor=white)](https://github.com/rachel-kim2255/Machine-Learning-Notebooks/blob/main/2_%5BLogistic_Regression%5D_Titanic_survival_prediction.ipynb)

> Logistic regression is a classification algorithm used for problems with two possible outcomes, such as Yes/No or Survived/Not Survived.  
In this project, I used a logistic regression model to analyze the Titanic dataset and predict passenger survival.  
This is a binary classification problem where the target variable indicates whether a passenger survived or not.

### Key Results
**Accuracy:** 78% (initial model) → 79.21% (after simple feature engineering)

*[Feb 2026]*

---

## 3. [KNN Model] Wine Class Prediction
[![Jupyter Notebook](https://img.shields.io/badge/Notebook-View%20on%20GitHub-orange?logo=jupyter&logoColor=white)](https://github.com/rachel-kim2255/Machine-Learning-Notebooks/blob/main/3_%5BKNN_Model%5D_Wine_Class_Prediction_.ipynb)

> In this project, I used a KNN (K-Nearest Neighbors) model to classify wines into three quality classes (0, 1, 2) based on 13 chemical features such as alcohol content, flavanoids, and color intensity.
KNN is a distance-based algorithm that predicts the class of a new data point by majority voting among its K nearest neighbors.
Since the features had significantly different scales, MinMax Scaling was applied before training to ensure fair distance calculations.

### **Key Results**

**1) Best Accuracy: 97.2% (n_neighbors = 13)**
- The model was tested with n_neighbors ranging from 1 to 20, and the highest accuracy of 97.2% was achieved at K = 13, 18, and 20.
- K = 13 was selected as the optimal parameter since it produces the same accuracy with less computation.

**2) Baseline Accuracy: 88.9% (default K = 5)**
- With the default setting of K = 5, the model achieved 88.9% accuracy.
- Hyperparameter tuning improved performance by approximately 8.3 percentage points.

**3) Impact of Scaling**
- Variables such as `proline` (range: 278–1,680) and `alcohol` (range: 11–14.75) had vastly different scales.
- Applying MinMax Scaling was essential to prevent larger-scale features from dominating distance calculations.

*[2026-Mar]*


---

## 4. [Naive Baise] Filtering Spam Messages
[![Jupyter Notebook](https://img.shields.io/badge/Notebook-View%20on%20GitHub-orange?logo=jupyter&logoColor=white)](https://github.com/rachel-kim2255/Machine-Learning-Notebooks/blob/main/4_%5BNaive_Bayes%5D_Filtering_Spam_Messages.ipynb)

In this project, I used a Naive Bayes model to classify whether emails are spam or not. 
Naive Bayes assumes that each feature is independent and calculates probabilities for classification. 
Using this approach, the model predicts whether a message belongs to the spam or non-spam (ham) category.
### **Key Results**
**1) Accuracy: 98.6%**  
- Out of 1,115 total emails, the model correctly classified 1,099 emails (965 + 134).

**2) Precision: 134 / (134 + 12) ≈ 91.8%**  
- Among the emails predicted as spam, 91.8% were actually spam.  
- However, 12 normal emails were mistakenly classified as spam.

**3) Recall: 134 / (134 + 4) ≈ 97.1%**  
- Among the actual spam emails, the model successfully detected 97.1% of them, missing only 4 spam emails.

*[2026-Mar]*



---

<br>
<br>
<br>
<br>




---

### **References**
* **Main Textbook**: This project follows the examples and methodology from **"데싸노트의 실전에서 통하는 머신러닝"** (Machine Learning for Real-world Practices) by Sihyeon Kwon, published by Golden Rabbit (2022).
* **Official Repository**: [Golden Rabbit Must-Have ML-10](https://github.com/musthave-ML10)
