# 🚢 Titanic Survival Prediction
This project uses the Kaggle Titanic dataset to predict passenger survival using Logistic Regression and Random Forest Classifier. 

## 🧭 Process Overview
-  Exploratory Data Analysis (EDA)
-  Data Cleaning
      - Imputed missing 'Age' values using median per Pclass
      - Dropped the 'Cabin' column (since it had too many missing values)
-  Feature Engineering
      - Converted categorical variables (Sex, Embarked) into numeric dummy variables with pd.get_dummies()
      - Dropped irrelevant features (Name, Ticket, PassengerId)
-  Model Building
      -  Logistic Regression
      -  Random Forest Classifier
-  Prediction on Test dataset
     - Applied the same preprocessing pipeline to test.csv
     - Generated predictions using both models
     - Saved results into all_predictions.csv


## 📊 Results
| Model               | Accuracy | Precision (0) | Recall (0) | F1 (0) | Precision (1) | Recall (1) | F1 (1) |
| ------------------- | -------- | ------------- | ---------- | ------ | ------------- | ---------- | ------ |
| Logistic Regression | **0.83** | 0.82          | **0.92**   | 0.87   | **0.85**      | 0.69       | 0.76   |
| Random Forest       | **0.82** | **0.84**      | 0.88       | 0.86   | 0.79          | **0.73**   | 0.76   |

- Logistic Regression achieved ~83% accuracy, with higher recall for non-survivors (0.92), but lower recall for survivors (0.69, giving slightly better predictions in terms of overall accuracy & recall for non-survivors
- Random Forest achieved ~82% accuracy, with a more balanced precision–recall tradeoff between survivors and non-survivors
- Both models’ predictions were saved for comparison in all_predictions.csv
