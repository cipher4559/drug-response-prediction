#  Drug Response Prediction App

##  Project Overview
The **Drug Response Prediction App** is an AI-powered tool designed to predict the likely response of cancer patients to specific drug treatments.  
Leveraging machine learning, this application supports **personalized treatment planning** by providing actionable insights based on patient demographics, tumor characteristics, and biomarker profiles.  

This tool is ideal for:
- Clinicians and oncologists for treatment decision support  
- Healthcare researchers analyzing patient response trends  
- Data scientists exploring predictive modeling in oncology  

---

##  Key Features

### Single Patient Prediction
- Input details for an individual patient:
  - Age  
  - Sex  
  - Tumor Size (mm)  
  - Biomarker Status (Positive/Negative)  
- Get an immediate prediction for drug response.

### Batch Prediction
- Upload CSV files containing multiple patient records.  
- Automatically predicts responses for all entries and outputs results in a structured table.  
- Includes validation to ensure required columns exist and inputs are standardized.  

### Robust & User-Friendly
- Handles missing or misformatted categorical inputs automatically.  
- One-hot encodes features to align with the trained model.  
- Interactive **Gradio web interface** for seamless usage.  

---

##  Technology Stack

| Component               | Technology / Library |
|-------------------------|--------------------|
| Programming Language    | Python 3.x         |
| Machine Learning Model  | Random Forest Classifier |
| Data Processing         | pandas, numpy      |
| Model Training & Encoding | scikit-learn, imbalanced-learn, joblib |
| Explainability          | SHAP               |
| Web Interface           | Gradio             |
| Version Control         | Git & GitHub       |

---

##  How It Works

1. **Preprocessing**
   - Categorical features (`Sex`, `Biomarker_Status`) are one-hot encoded.  
   - Target variable is label-encoded for model training.

2. **Model Training**
   - Random Forest Classifier trained on historical patient data.  
   - Class imbalance handled via oversampling for better prediction accuracy.

3. **Prediction**
   - **Single Prediction:** Normalizes input and aligns features with training columns.  
   - **Batch Prediction:** Validates CSV, normalizes categorical columns, aligns with model columns, and outputs predictions.  

---

##  Usage

### Single Prediction
1. Launch the Gradio app.  
2. Navigate to **Single Prediction** tab.  
3. Enter patient details (Age, Sex, Tumor Size, Biomarker Status).  
4. Click **Predict Response** to view the predicted outcome.

### Batch Prediction
1. Navigate to **Batch Prediction** tab.  
2. Upload a CSV file with the following columns:  
   `Age`, `Tumor_Size`, `Sex`, `Biomarker_Status`  
3. The app validates the input and outputs predictions in a table with an additional column: `Predicted_Response`.

---

##  Sample CSV Format

| Age | Tumor_Size | Sex    | Biomarker_Status |
|-----|------------|--------|-----------------|
| 50  | 20.0       | Male   | Positive        |
| 60  | 15.5       | Female | Negative        |

---

## Installation

```bash
# Clone the repository
git clone https://github.com/cipher4559/drug-response-prediction.git
cd drug-response-prediction

# Install required packages
pip install -r requirements.txt

# Run the app
python drug_responce.py
```
 Project Impact
Accelerates drug response assessment for cancer patients

Enables personalized and data-driven treatment strategies

Reduces trial-and-error in treatment planning

 Author
Cipher (Manikanta Reddy Maguluri)

Email: mmkr4559@gmail.com

GitHub: https://github.com/cipher4559

📜 License
This project is licensed under the MIT License. See the LICENSE file for details
