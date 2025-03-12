# Hydrate Formation Temperature Prediction Model

## Overview
The idea of ​​the model is to convert the hydrate curve to a ML model and use it.
This machine learning project predicts hydrate formation temperature using pressure and gas density measurements. The model employs various regression algorithms to achieve accurate predictions, which is crucial for preventing hydrate blockages in oil and gas pipelines.

## Features
- **Input Features**: Pressure (psi), Gas Density (g/cc)
- **Target Variable**: Temperature (°F)
- **Algorithms Tested**:
  - Linear Regression
  - Decision Tree
  - Support Vector Regressor (SVR)
  - Random Forest
  - Gradient Boosting

## Model Performance
| Model               | Train R²   | Test R²    | Train RMSE | Test RMSE |
|---------------------|------------|------------|------------|-----------|
| Linear Regression   | 0.708      | 0.719      | 7.008      | 6.995     |
| Decision Tree       | 1.000      | 0.999      | 0.000      | 0.196     |
| SVR                 | 0.912      | 0.922      | 3.847      | 3.688     |
| Random Forest       | **0.999      | 0.999      | 0.052      | 0.125** |
| Gradient Boosting   | 0.999      | 0.999      | 0.272      | 0.377     |

### Key Insights:
- **Best Performers**: Random Forest and Gradient Boosting achieved near-perfect scores (R² > 0.999), indicating excellent predictive capability.  Random Forest was ultimately chosen due to slightly lower RMSE.
- **Overfitting Alert**: Decision Tree demonstrates perfect training accuracy, suggesting potential overfitting on the training data despite high test performance.
- **Baseline Model**: Linear Regression serves as a reasonable baseline, providing a basic level of prediction accuracy (R² ~0.71) against which to compare more complex models.

## Technical Details
- **Dataset**: Proprietary experimental data from oil/gas operations.  This dataset is *not publicly shared* due to confidentiality.
- **Data Split**: 60% training, 20% validation, 20% test split. A validation set was used for hyperparameter tuning and preventing overfitting.
- **Evaluation Metrics**: R-squared (R²) and Root Mean Squared Error (RMSE) were used to assess model performance.
- **Key Libraries**: Python, Pandas, NumPy, Scikit-learn, Matplotlib

## How to Use (Conceptual)
This model, if made available, would ideally be integrated into a pipeline simulation or process control system using its API:

1. Input the pressure and gas density measurements.
2. The model predicts hydrate formation temperature.
3. The temperature prediction assists the user in maintaining temperature.


## Applications
- Flow assurance in oil/gas pipelines
- Process optimization in hydrocarbon production
- Safety system design for subsea operations

---
*Note: Data are available.*
