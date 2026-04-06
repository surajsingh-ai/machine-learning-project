# Heart Disease Prediction – Machine Learning Project

This repository contains a **machine learning** web app built with Streamlit to predict the risk of heart disease based on medical attributes. The app loads a pre-trained K-Nearest Neighbors (KNN) model along with saved preprocessing objects (scaler and column mappings) to generate predictions in real time.

## Features

- Interactive Streamlit UI for entering patient health parameters
- Uses a trained KNN classifier for heart disease prediction
- Preprocessing handled via pre-fitted scaler and column encodings
- Simple deployment-ready structure (single `app.py` + model artifacts)

## Project Structure

```
.
├── app.py               # Streamlit application
├── knn_heart_model.pkl  # Trained KNN model
├── heart_scaler.pkl     # Fitted scaler for numerical features
├── heart_columns.pkl    # Feature/column order used during training
├── requirements.txt     # Python dependencies
├── .gitignore
└── README.md
```

## Installation

1. Clone the repository:

```bash
git clone https://github.com/surajsingh-ai/machine-learning-project.git
cd machine-learning-project
```

2. (Optional but recommended) Create and activate a virtual environment:

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

If needed, you can also install them manually:

```bash
pip install streamlit pandas scikit-learn joblib numpy
```

## Usage

Run the Streamlit app:

```bash
streamlit run app.py
```

Then open the URL shown in the terminal (usually `http://localhost:8501`) in your browser.
Enter the patient's health information in the form and click the **Predict** button to see the model's output.

## Model Details

- **Algorithm:** K-Nearest Neighbors (KNN) classifier (classification for heart disease: risk vs no risk)
- **Input:** Typical heart disease dataset features (e.g., age, sex, chest pain type, blood pressure, cholesterol, etc.)
- **Preprocessing:**
  - Numerical features scaled using `heart_scaler.pkl`
  - Column order and feature mapping stored in `heart_columns.pkl`

> **Note:** The training notebook/dataset can be added later (e.g., `notebooks/` or `data/`) if you want to show the complete ML workflow.

## Requirements

The main libraries are:

```txt
streamlit==1.53.0
pandas>=1.4.0
scikit-learn>=1.0.0
joblib>=1.3.0
numpy>=1.23.0
```

(Also listed in `requirements.txt`.)

## How to Contribute

- Fork this repository
- Create a new branch for your feature or bugfix
- Commit your changes with clear messages
- Open a pull request describing your changes

## Future Improvements

- Add training code and Jupyter notebooks
- Include evaluation metrics and visualizations (ROC curve, confusion matrix)
- Add authentication or user management
- Deploy the app on cloud platforms (Streamlit Community Cloud, Render, etc.)

Deployed app: [https://machine-learning-project-2-onop.onrender.com/](https://machine-learning-project-2-onop.onrender.com/)


## License

MIT License – feel free to use and modify this project for your learning purposes.
