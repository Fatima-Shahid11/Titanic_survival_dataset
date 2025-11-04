# 🚢 Titanic Survival Prediction

## 🧭 Introduction
The Titanic Survival Prediction project aims to predict whether a passenger survived the Titanic disaster using machine learning techniques.  
This is a classic binary classification problem where the target variable is **Survived** (1 = Survived, 0 = Did Not Survive).

---

## 🎯 Objective
The main objective is to develop a predictive model that can accurately determine the survival of passengers based on their demographic and travel information.

---

## 📂 Dataset Description
The dataset is derived from the [Kaggle Titanic competition](https://www.kaggle.com/c/titanic).  
It contains information about passengers such as:

---

## 🧹 Data Preprocessing

### 1. Handling Missing Values
- Missing **Age** values are filled using the **median** of the column.  
- Missing **Embarked** values are filled using the **mode** (most frequent value).  
- Missing **Fare** values are filled using the **median**.  

### 2. Encoding Categorical Variables
- **Sex** and **Embarked** columns are converted into numeric form using **one-hot encoding** to make them compatible with the machine learning model.

### 3. Feature Selection
The most relevant features for prediction are selected:
- Pclass  
- Age  
- SibSp  
- Parch  
- Fare  
- Sex (encoded)  
- Embarked (encoded)

---

## 🧠 Model Selection
A **Random Forest Classifier** is chosen due to its:
- Ability to handle both numerical and categorical data  
- Robustness to overfitting  
- Strong performance with minimal tuning  

---

## ⚙️ Model Training and Validation
- The dataset is split into **training** (80%) and **validation** (20%) sets.  
- The model is trained on the training set and evaluated on the validation set using **accuracy** as the performance metric.

---

## 📈 Evaluation
- The Random Forest model achieves an accuracy of approximately **80%** on the validation set.  
- This indicates that the model can generalize well to unseen data.

---

## 📁 Output
After training, the model is used to generate predictions for the **test dataset**.  
These predictions are saved in a file named **`submission.csv`**, which contains:

| Column | Description |
|---------|--------------|
| **PassengerId** | Unique passenger identifier |
| **Survived** | Predicted survival (0 or 1) |

---

## 🧩 Dependencies
| Library | Purpose |
|----------|----------|
| **pandas** | Data manipulation and preprocessing |
| **matplotlib** | Data visualization |
| **seaborn** | Statistical data visualization |
| **scikit-learn** | Machine learning model building and evaluation |
