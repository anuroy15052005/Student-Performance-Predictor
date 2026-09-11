# Student Exam Performance Predictor

An end-to-end machine learning project that predicts a student's math score based on demographic and academic attributes. Built with a modular, production-style pipeline and deployed as a Flask web application.

## Overview

This project takes inputs such as gender, ethnicity, parental education level, lunch type, test preparation course status, and reading/writing scores, and predicts the student's math score using a trained regression model.

## Features

- Modular ML pipeline (data ingestion → transformation → model training → prediction)
- Multiple regression models trained and compared, including CatBoost and XGBoost
- Custom prediction pipeline for handling new user input
- Simple web interface built with Flask, HTML, and CSS
- Serialized model and preprocessing objects for fast inference

## Tech Stack

- **Language:** Python
- **ML Libraries:** scikit-learn, CatBoost, XGBoost
- **Data Handling:** pandas, NumPy
- **Visualization (EDA):** matplotlib, seaborn
- **Web Framework:** Flask
- **Serialization:** dill

## Project Structure

```
mlproject/
├── artifacts/          # Saved model and preprocessor objects
├── notebook/           # EDA and model experimentation notebooks
├── src/                # Source code (pipeline, components, utils)
├── static/css/         # Stylesheets for the web app
├── templates/          # HTML templates
├── app.py              # Flask application entry point
├── requirements.txt    # Project dependencies
└── setup.py            # Package setup
```

## How It Works

1. **Data Ingestion & Transformation** — Raw data is cleaned, encoded, and scaled.
2. **Model Training** — Several regression models are trained and evaluated; the best-performing model is saved to `artifacts/`.
3. **Prediction Pipeline** — New input data is transformed using the saved preprocessor and passed to the saved model for prediction.
4. **Web App** — Users enter their details through a form; the app returns a predicted math score.

## Running Locally

```bash
git clone https://github.com/anuroy15052005/mlproject.git
cd mlproject
pip install -r requirements.txt
python app.py
```

Then visit `http://localhost:5000` in your browser.

## Deployment

This project is deployed on [Render](https://render.com) using Gunicorn as the production server.

## Author

**Anu Roy**
GitHub: [@anuroy15052005](https://github.com/anuroy15052005)