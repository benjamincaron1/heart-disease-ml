# Heart Disease Prediction using Machine Learning by Benjamin CARON

#Objective

This project aims to build a machine learning model capable of predicting whether a patient has heart disease based on medical attributes.

#Dataset

The dataset used is the **UCI Heart Disease dataset (Cleveland)**.

It contains medical features such as:
* Age
* Sex
* Chest pain type (`cp`)
* Cholesterol (`chol`)
* Maximum heart rate (`thalach`)
* And more...

##Target variable

* `0` → No heart disease
* `1` → Presence of heart disease

> Note: The original dataset had values from 0 to 4. These were converted into a binary classification problem.

#Project Workflow

1. **Data Loading**
2. **Data Cleaning**

   * Handling missing values (`?`)
   * Converting data types
3. **Exploratory Data Analysis (EDA)**

   * Distribution plots
   * Correlation heatmap
4. **Feature Engineering**
5. **Model Training**

   * Logistic Regression
   * Random Forest
6. **Evaluation**

   * Accuracy
   * Confusion Matrix
   * Classification Report
   * ROC Curve & AUC

#Models Used

##Logistic Regression

* Accuracy: **0.88**
* Recall (disease): **0.88**
* AUC: **0.947**

#Model Optimization

The classification threshold was adjusted from **0.5 → 0.3** to improve detection of heart disease.

##Result:

* Recall improved to **0.92**
* Slight decrease in precision and accuracy

> This trade-off is acceptable in medical contexts where missing a patient is more critical than false alarms.

---

#Key Insights

* Chest pain type (`cp`) is highly correlated with heart disease
* Maximum heart rate (`thalach`) shows negative correlation
* ST depression (`oldpeak`) is a strong indicator
* Number of vessels (`ca`) is highly predictive

#Evaluation Metrics

* **Accuracy**: Overall correctness
* **Precision**: Reliability of positive predictions
* **Recall**: Ability to detect actual cases (critical in healthcare)
* **F1-score**: Balance between precision and recall
* **AUC (0.947)**: Excellent model discrimination ability

#Conclusion

The model demonstrates strong performance in predicting heart disease, with high accuracy and excellent AUC.

Adjusting the classification threshold improves sensitivity, making the model more suitable for real-world medical screening scenarios.

#Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

#Project Structure

heart-disease-ml-project/
│
├── data/
├── notebooks/
├── src/
├── models/
├── reports/
├── README.md
├── requirements.txt
└── .gitignore

#Future Improvements

* Hyperparameter tuning (GridSearchCV)
* Try advanced models (XGBoost, SVM)
* Deploy model as a web app (Streamlit)
* Use larger datasets
