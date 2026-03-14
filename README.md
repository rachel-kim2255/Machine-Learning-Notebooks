# Machine-Learning-Notebooks
Documenting my journey through Machine Learning. This repository features step-by-step implementations of various models, from Linear Regression to Advanced Boosting techniques.

---
## 1. [Linear Model] Predicting Insurance Premiums
[![Jupyter Notebook](https://img.shields.io/badge/Notebook-View%20on%20GitHub-orange?logo=jupyter&logoColor=white)](https://github.com/rachel-kim2255/Machine-Learning-Notebooks/blob/main/1_%5BML_Linear_Model%5D_Predicting_Insurance_Premiums.ipynb)

> In this project, I used a Linear Regression model to predict individual insurance charges based on demographic and health indicators such as age, BMI, and smoking status.
Linear Regression finds the best-fitting line that explains the relationship between independent variables and the target variable.
Using this approach, the model estimates insurance costs based on each individual's profile.

### **Key Results**

**1) R-squared: 73.6%**
- The model explains approximately 73.6% of the variance in insurance premiums, indicating solid predictive power.

**2) RMSE: 5,684**
- The model's average prediction error is approximately 5,684.
- Since RMSE is relative to the scale of the target variable, this value serves as a baseline for comparing against other models.

**3) Most Influential Feature: Smoker**
- Smoking status had by far the largest impact, with smokers incurring approximately $23,469 more in charges than non-smokers.
- Age (+$264.8 per year) and BMI (+$297.5 per unit) also showed positive correlations with insurance costs.

*[2026-Jan]*

---

## 2. [Logistic Regression] Titanic Survival Prediction
[![Jupyter Notebook](https://img.shields.io/badge/Notebook-View%20on%20GitHub-orange?logo=jupyter&logoColor=white)](https://github.com/rachel-kim2255/Machine-Learning-Notebooks/blob/main/2_%5BLogistic_Regression%5D_Titanic_survival_prediction.ipynb)

> In this project, I used a Logistic Regression model to predict whether a passenger survived the Titanic disaster based on features such as passenger class, age, sex, and embarkation port.
Logistic Regression is a classification algorithm used for binary outcomes, predicting the probability of survival (1) or not (0).
Feature engineering was also applied to reduce multicollinearity and improve model performance.

### **Key Results**

**1) Accuracy: 79.2% (after feature engineering)**
- The baseline model achieved 78.1% accuracy.
- After combining `SibSp` and `Parch` into a single `family` feature to address multicollinearity, accuracy improved to 79.2%.

**2) Most Influential Feature: Sex**
- Sex had the largest impact with a coefficient of −2.57, indicating that female passengers had a significantly higher probability of survival.
- Passenger class (−1.18) was the second most influential factor, where lower class numbers (1st class) were associated with higher survival rates.

**3) Feature Engineering: Creating the `family` Variable**
- Since `SibSp` and `Parch` showed a moderate correlation (0.41), they were combined into a new `family` variable representing total family members aboard.
- This reduced multicollinearity and contributed to the improvement in model accuracy.


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

> In this project, I used a Naive Bayes model to classify whether emails are spam or not.
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
