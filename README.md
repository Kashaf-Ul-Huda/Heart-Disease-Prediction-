# Heart Disease Prediction

## Objective
Predict the presence of heart disease using patient clinical data. The project demonstrates data preprocessing, feature engineering, model training, evaluation, and deployment using Gradio.

## Dataset
- **Source:** Kaggle – [Heart Disease Prediction by Rishi Damarla](https://www.kaggle.com/datasets/rishidamarla/heart-disease-prediction)
- **Description:** Contains clinical features such as age, sex, blood pressure, cholesterol, fasting blood sugar, ECG results, max heart rate, exercise induced angina, ST depression, slope, number of major vessels, thalassemia.
- **Target:** Heart disease indicator (1 = presence, 0 = absence)

## Methodology
1. **Load the Dataset**
   - Read CSV using pandas.
   - Printed `head()`, `info()`, and checked for missing values.
   - Removed trailing spaces from column names using `df.columns.str.strip()`.

2. **Data Preprocessing**
   - Handled missing values by imputing median for numeric columns.
   - Scaled features using `StandardScaler` for better model performance.

3. **Feature Selection**
   - All clinical features were used as inputs.
   - Target variable: Heart disease label.

4. **Train-Test Split**
   - 80% training, 20% testing.

5. **Modeling**
   - Random Forest Classifier (100 estimators)
   - Logistic Regression (optional for comparison)
   - Model trained on training data.

6. **Evaluation**
   - Accuracy, confusion matrix, classification report.
   - Random Forest achieved **~85–90% accuracy** (depending on dataset version).

7. **Visualization**
   - Heatmap of correlations
   - Distribution of target variable

8. **Gradio Deployment**
   - User inputs clinical features.
   - Output: “Heart Disease” or “No Heart Disease”.
   - Uses trained model and scaler for prediction.

## Results
- Random Forest performed best for prediction.
- Gradio interface allows interactive testing for hypothetical patients.

## References
- Kaggle Dataset: [Heart Disease Prediction](https://www.kaggle.com/datasets/rishidamarla/heart-disease-prediction)
- Python Libraries: pandas, scikit-learn, numpy, gradio
