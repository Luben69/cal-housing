# California Housing Price Prediction

## Overview
This project explores the California Housing dataset and builds machine learning regression models to predict median house values.

## Methodology
- Exploratory data analysis (EDA)
- Comparison of baseline and regression models
- 5-fold cross-validation
- Hyperparameter tuning with GridSearchCV
- Feature importance and residual analysis
- Final evaluation on a held-out test set

## Final Model and Results
The tuned Random Forest achieved the following results on the test set:

| MAE | 0.326007 (~$32,600) |
| RMSE | 0.503828 (~$50,400) |
| R² | 0.806288 |

## Key Findings
- Median income (`MedInc`) was the strongest predictor in the feature-importance analyses.
- Geographic features (`Latitude` and `Longitude`) were also important.
- Residual analysis revealed a diagonal pattern associated with the dataset's $500,000 target-value cap.

## Limitations
- Target values are capped at approximately $500,000, limiting predictions for higher-value homes.
- Prediction errors remain substantial for some observations.
- Feature importance describes predictive usefulness, not causation.

## Conclusion
The tuned Random Forest captured a substantial amount of variation in median house values. The project demonstrates an end-to-end regression workflow, including exploratory analysis, model selection, evaluation, and interpretation.


## Installation

1. Clone the repository
git clone <https://github.com/Luben69/cal-housing>
cd cal-housing

2. Create a virtual environment
python -m venv .venv

Activate it:

Linux / macOS:
source .venv/bin/activate

Windows:
.venv\Scripts\activate

3. Install dependencies
pip install -r requirements.txt

4. Run the notebook
jupyter notebook