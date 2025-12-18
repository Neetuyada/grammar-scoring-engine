# Grammar Scoring Engine from Voice Samples

This repository contains my solution for the **SHL Research Intern Assessment – Grammar Scoring Engine from Voice Samples**.  
The objective of this task is to predict grammar proficiency scores from spoken audio recordings using classical machine learning techniques.

---

## Problem Statement

Given a set of speech audio samples, the goal is to build a regression model that can predict a continuous grammar score for each audio file.  
The evaluation of the model is based on **RMSE** and **Pearson Correlation**, as defined in the Kaggle competition.

---

## Dataset Overview

- Audio files provided in `.wav` format
- Separate training and test datasets
- Training data includes:
  - `filename`
  - `label` (grammar score)
- Test data includes:
  - `filename` only

All datasets were accessed directly from the Kaggle competition environment.

---

## Approach

The solution follows a **simple, interpretable, and reproducible pipeline**, focusing on correctness and clarity rather than complexity.

### 1. Audio Preprocessing & Feature Extraction
- Loaded audio files using **Librosa**
- Extracted **MFCC (Mel-Frequency Cepstral Coefficients)** features
- Aggregated MFCC features using mean values to obtain fixed-length vectors

### 2. Model Selection
- Used **Linear Regression** from scikit-learn
- Chosen to maintain interpretability and avoid overfitting
- No deep learning models were used, as per task expectations

### 3. Training & Evaluation
- Model trained on extracted MFCC features
- Performance evaluated using **Root Mean Squared Error (RMSE)** on training data
- RMSE score is explicitly computed and reported in the notebook (mandatory requirement)

---

## Evaluation Metrics

- **RMSE (Root Mean Squared Error)** – Computed within the notebook
- **Pearson Correlation** – Used by the Kaggle leaderboard for final evaluation

---

## Visualizations

To ensure interpretability, the following plots are included in the notebook:

- **Actual vs Predicted Scores (Training Data)**
- **Distribution of Predicted Scores (Test Data)**

These visualizations help in understanding model behavior and prediction spread.

---

## Output

- Generated a `submission.csv` file containing:
  - `filename`
  - `label` (predicted grammar score)

This file was submitted directly to the Kaggle competition.

---

## Tools & Libraries Used

- Python
- NumPy
- Pandas
- Librosa
- Scikit-learn
- Matplotlib

---

## Notes

- The complete implementation, results, and explanations are provided in the Kaggle notebook.
- All code is well-documented and structured for clarity and reproducibility.
- This project was completed as part of an assessment and is intended for evaluation purposes only.

## Author

**Neetu Yadav**  
B.Tech Graduate  
SHL Research Intern Assessment Submission
