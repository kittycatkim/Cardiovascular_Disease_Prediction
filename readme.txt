Applied Deep Learning Project - Cardiovascular Disease Prediction
=================================================================

Project Overview:
-----------------
This project develops and evaluates multiple deep learning models to predict cardiovascular disease using tabular patient health data. 
It compares different architectures (varying in layers, dropout, optimizers) and incorporates model explainability techniques 
such as SHAP and LIME to interpret predictions.

Top Model:
----------
Model Name: Model_5_2_Layers_Adam_Lower_Dropout
 - Architecture: 2 hidden layers (64/32 neurons), ReLU activation
 - Optimizer: Adam, Learning Rate: 0.001, Dropout Rate: 0.1
 - Performance (Test Set):
    - F1 Score: 0.721
    - Balanced Accuracy: 0.731
    - AUC: 0.798
    - Precision: 0.748
    - Recall: 0.697
 - Training Time: ~275 seconds
 - Epochs to Converge: 28
 - Total Parameters: 2,689

Explainability:
---------------
SHAP:
 - Highlights systolic blood pressure (ap_hi), age, and cholesterol as top global predictors.
 - Shows feature-level influence across samples.

LIME:
 - Provides local explanation for individual predictions.
 - Top negative influencers (reducing risk): low smoking, low weight, younger age, low alcohol consumption, physical activity.


Usage:
------
1. Ensure all dependencies are installed: tensorflow, sklearn, lime, shap, matplotlib, pandas, numpy.
2. Run the notebook cell-by-cell to preprocess data, train models, evaluate results, and visualize explainability.
3. Modify hyperparameters in 'model_configs' to experiment with architectures.

Author:
-------
Cat Kim (UT Dallas)
