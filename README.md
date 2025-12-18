Project Summary: Earthquake Magnitude Prediction
1. Project Objective
The primary goal of this project was to build a robust machine learning model capable of predicting the Magnitude of earthquakes based on historical seismic data, including spatial and temporal features.

2. Data Preparation & Feature Engineering
To improve the model's predictive power, we performed significant feature engineering:

Temporal Features: Extracted Year, Month, Day, and Day of the Week from the Date column to capture seasonal or yearly patterns.

Interaction Features: Created a Depth_Mag_Ratio to help the model understand the relationship between the depth of an earthquake and its magnitude.

Data Cleaning: Handled datetime conversions and addressed null values to ensure a clean input for the algorithm.

3. Methodology
Algorithm: We utilized the Random Forest Regressor, an ensemble learning method known for its stability and ability to handle non-linear relationships.

Optimization: Employed RandomizedSearchCV for hyperparameter tuning to find the most efficient settings for the model.

Validation: Used K-Fold Cross-Validation (5 folds) to ensure the model performs consistently across different subsets of the data and is not overfitting.

4. Key Performance Metrics
The model showed a massive improvement after feature engineering and tuning:

Baseline RMSE: 14.65 (Initial model with default settings).

Final Improved RMSE: 0.083 (Highly accurate).

Cross-Validation Mean RMSE: 0.082, confirming the model's reliability and stability.

5. Visual Insights
Actual vs. Predicted Plot: The scatter points align closely with the 45-degree identity line, indicating high precision.

Residual Analysis: The errors are randomly distributed around the zero-line, showing no significant bias in the predictions.

Distribution Overlap: The KDE plot shows an almost perfect overlap between the actual and predicted magnitude distributions.

6. Final Conclusion
The final model is highly optimized and ready for deployment. It has been saved as a .pkl file for future use. The extremely low RMSE suggests that the engineered features provided the model with enough information to predict magnitudes with near-perfect accuracy on this specific dataset.