# Placement Predictor

A web application that estimates a student's chance of being placed in on-campus recruitment, based on details such as stream, CGPA, internships and backlogs. The student fills in a short form and a trained machine learning model returns the prediction.

Team project, Bachelor of Engineering (Computer Engineering), A. P. Shah Institute of Technology.

## How it works

1. A Random Forest classifier is trained on a public placement dataset from Kaggle (`collegePlace.csv`).
2. The trained model is saved and loaded by a Flask app.
3. The user enters their details in a form, and the app returns the predicted placement outcome.

An SVM model was also trained for comparison (`svm.ipynb`).

## Results

The Random Forest model reached 88% accuracy and 94% precision on held-out data.

## Tech stack

Python, scikit-learn, pandas, Flask, HTML, CSS, Jupyter Notebook

## Project structure

| File | Purpose |
| --- | --- |
| `collegePlace.ipynb` | Data exploration and Random Forest training |
| `svm.ipynb` | SVM model for comparison |
| `model.py` | Model training script |
| `app.py` | Flask web app |
| `templates/` | Input form and result pages |
| `static/` | CSS and images |
| `ml_miniproject_report.pdf` | Project report |

## Run it locally

```bash
git clone https://github.com/Kars28/placement-predictor.git
cd placement-predictor
pip install -r requirements.txt
python app.py
```

Then open http://127.0.0.1:5000 in your browser.
