# Analytics in Healthcare: Breast Cancer Prediction

## Project Overview

This project applies machine learning to predict whether a breast tumor
is **benign or malignant** using measurements extracted from digitized
fine-needle aspiration (FNA) images of breast masses. The features
describe characteristics of cell nuclei.

The project explores data analysis, feature selection, ensemble
classification models, and model evaluation. A Streamlit web application
is also provided as a deployment demo.

> **Disclaimer:** This project is for educational purposes only. It is
> not a medical device and must not be used for diagnosis or treatment
> decisions.

## Problem Statement

Build a classification model that uses tumor measurement features to
predict the diagnosis class (benign or malignant).

## Machine Learning Workflow

1.  Load the dataset and inspect its structure.
2.  Clean and prepare the data.
3.  Perform exploratory data analysis and examine feature relationships.
4.  Select the five features identified in the notebook using
    `SelectKBest` with the chi-squared test:
    -   `texture_mean`
    -   `area_mean`
    -   `concavity_mean`
    -   `area_se`
    -   `concavity_worst`
5.  Split the data into training and testing sets using a 70:30 split
    (`test_size=0.30`, `random_state=10`).
6.  Train and compare ensemble classification models.
7.  Evaluate model performance using a confusion matrix, classification
    report, ROC curve/AUC, precision, recall, accuracy, and F1-score.

## Models Explored in the Notebook

-   Random Forest Classifier
-   Bagging Classifier (with a decision-tree base estimator)
-   AdaBoost Classifier
-   XGBoost Classifier

The notebook's result discussion reports that AdaBoost performed better
than the other evaluated models for its chosen metrics. Refer to the
notebook's model-comparison output for the detailed metric values.

## Streamlit Deployment Demo

The repository's `app.py` is a lightweight deployment demo. It trains a
Random Forest model using the Wisconsin Breast Cancer dataset bundled
with scikit-learn and accepts five input measurements through a
Streamlit interface.

**Important:** The Streamlit demo is not an exact deployment of every
experiment in the original notebook. It uses scikit-learn's built-in
dataset and five selected features so it can run without a local
`cancer.csv` file. Its displayed test accuracy is calculated when the
app starts; it is not a claim of clinical performance.

## Repository Structure

``` text
analytics-healthcare/
├── app.py
├── requirements.txt
├── README.md
└── Analytics in Healthcare.ipynb  # optional: add the original notebook
```

## Run Locally

### 1. Clone the repository

``` bash
git clone https://github.com/YOUR-USERNAME/analytics-healthcare.git
cd analytics-healthcare
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Install dependencies

``` bash
python -m pip install -r requirements.txt
```

### 3. Start the app

``` bash
streamlit run app.py
```

Streamlit will print a local URL (usually `http://localhost:8501`) in
the terminal.

## Deploy on Render Using GitHub

1.  Push `app.py`, `requirements.txt`, and `README.md` to the root of a
    GitHub repository.
2.  Sign in to [Render](https://dashboard.render.com/).
3.  Choose **New + → Web Service** and connect your GitHub repository.
4.  Configure the service:
    -   **Runtime:** Python 3
    -   **Build command:** `pip install -r requirements.txt`
    -   **Start command:**
        `streamlit run app.py --server.port $PORT --server.address 0.0.0.0`
5.  Choose an available instance plan and create the Web Service.
6.  When deployment completes, open the public URL provided by Render.

Render may take a little time to install the Python packages and start
the service.

## Dependencies

The deployment demo requires:

-   Python
-   Streamlit
-   pandas
-   scikit-learn

These packages are listed in `requirements.txt`.

## Limitations

-   The app is an educational prototype, not a clinically validated
    tool.
-   Predictions depend on the training dataset and the selected
    features.
-   The demo model and dataset are separate from the full
    model-comparison workflow in the original notebook.
-   Do not enter identifiable or confidential patient information.

## Future Improvements

-   Deploy the exact best-performing model trained in the notebook.
-   Add a reproducible data-preparation and model-training pipeline.
-   Include validation results and model-comparison metrics in the web
    interface.
-   Add automated tests and document the dataset source and license.

## Author

Add your name, GitHub profile, and project links here.
