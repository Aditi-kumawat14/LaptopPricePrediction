# Laptop Price Prediction | End-to-End Machine Learning

An end-to-end Machine Learning application that predicts laptop prices in Indian Rupees (INR) based on laptop specifications. The project uses data preprocessing and regression models to generate price estimates through an interactive Streamlit web application.

## Project Overview

Laptop prices vary depending on specifications such as processor, RAM, storage, brand, and other hardware features.

This project aims to estimate laptop prices using Machine Learning by analyzing laptop specifications and identifying patterns in the dataset.

The trained model is integrated into a Streamlit application where users can enter laptop specifications or upload a CSV file to generate price predictions.

## Key Features

- Machine Learning-based laptop price prediction
- Numerical and categorical feature preprocessing
- Missing value imputation
- Feature scaling and One-Hot Encoding
- Linear Regression and Random Forest model comparison
- Model evaluation using MAE, RMSE, and R² score
- Saved model and preprocessing artifacts
- Interactive single-laptop price prediction
- Batch prediction using CSV upload
- Downloadable prediction results
- Streamlit web application

## Technologies Used

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Model Storage | Joblib |
| Database | MySQL |
| Web Framework | Streamlit |
| Version Control | Git, GitHub |

## Project Workflow

1. **Data Ingestion:** Load laptop data from MySQL or a local CSV file.
2. **Data Validation:** Validate the dataset and remove duplicate records.
3. **Data Preprocessing:** Handle missing values and prepare numerical and categorical features.
4. **Feature Transformation:** Apply scaling and One-Hot Encoding.
5. **Model Training:** Train and compare regression models.
6. **Model Evaluation:** Evaluate model performance using MAE, RMSE, and R².
7. **Model Saving:** Store the trained model and preprocessing artifacts.
8. **Prediction:** Generate laptop price estimates using Streamlit.

## Streamlit Application

The application provides two prediction options:

### 1. Single Laptop Prediction

- Enter laptop specifications through the application.
- Select categorical features and enter numerical values.
- Generate an estimated laptop price.
- Download the prediction result as a CSV file.

### 2. Batch Laptop Prediction

- Upload a CSV file containing multiple laptop specifications.
- Preview the uploaded dataset.
- Generate predictions for multiple laptops.
- Download the results as a CSV file.

## Repository Structure

```text
LaptopPricePrediction/
│
├── app.py
├── README.md
├── requirements.txt
├── .gitignore
│
├── artifacts/
│   └── transformed/
│       ├── preprocessor.joblib
│       ├── feature_list.json
│       └── train.csv
│
└── prediction/
    └── models/
        └── current_model.joblib
```

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Aditi-kumawat14/LaptopPricePrediction.git
cd LaptopPricePrediction
```

### 2. Create a Virtual Environment

**Windows:**

```powershell
python -m venv .venv
.venv\Scripts\activate
```

**macOS/Linux:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Run the Application

```bash
streamlit run app.py
```

The application will open in your default browser.

## Model Artifacts

The application uses previously generated Machine Learning artifacts:

| Artifact | Purpose |
|---|---|
| `current_model.joblib` | Trained model used for price prediction |
| `preprocessor.joblib` | Applies the required preprocessing transformations |
| `feature_list.json` | Stores numerical and categorical feature information |
| `train.csv` | Provides training feature data for default values and categorical options |

These files are required for the Streamlit application to perform predictions.

## Deployment

The application is deployed using Streamlit Community Cloud.

Deployment configuration:

- **Repository:** Aditi-kumawat14/LaptopPricePrediction
- **Branch:** main
- **Main file:** app.py

The application loads the saved model and preprocessing artifacts directly from the repository.

## Limitations

- Prediction accuracy depends on the quality and coverage of the training dataset.
- Estimated prices may differ from actual market prices.
- Predictions depend on the features provided by the user.
- Model performance may change when new laptop models and market trends emerge.

## Future Improvements

- Add more laptop specifications and updated market data.
- Improve prediction accuracy through model optimization.
- Add model explainability to understand feature contributions.
- Monitor prediction performance using new data.

## Author

**Aditi Kumawat**

- GitHub: https://github.com/Aditi-kumawat14

---

If you find this project useful, feel free to explore the repository and share your feedback.
