# Analysis-of-Metal-Alloy-Spectra-for-Elemental-Concentration-Prediction


This project focuses on utilizing Laser-Induced Breakdown Spectroscopy (LIBS) as an innovative method for analyzing metal alloys and trace elements. LIBS utilizes a laser to induce atomic emission properties, allowing for the examination of the elemental composition of samples. By detecting emitted photons with a spectrometer, valuable information regarding wavelengths and signal intensities is obtained. This non-destructive and highly sensitive approach holds significant promise across various fields, ranging from agriculture to environmental analysis.

## Objective
The primary objective of this study is to utilize atomic spectra acquired through LIBS as inputs for machine learning models to accurately predict elemental concentrations. The project aims to develop both linear regression and Partial Least Squares (PLS) models capable of predicting the elemental concentrations of the tested samples. Furthermore, the reliability and accuracy of these predictive models are evaluated through a series of rigorous tests.

## Methodology
The project begins with data collection and preparation, including the import and reading of files containing concentrations and test values. A list of 25 metal substances is created, followed by the definition of fundamental functions:
1. The "get_element_concentration" function retrieves the concentration of a specified element in the dataset.
2. The "prepare_datasets" function prepares training and testing datasets for analyzing the concentration of a particular element.

Following data preparation, a reduction in the number of rows is observed due to the exclusion of certain alloys with missing concentration values. Subsequently, two tuples are created:
- Training: consisting of pairs of spectral data and corresponding concentration values for model training.
- Testing: containing spectral data and actual concentration values for model evaluation.

The "create_model" function serves as the engine for training and evaluating machine learning models to predict element concentrations. It accepts several arguments, including the model type and the element of interest, and returns the trained model, R-squared score, and RMSE value.

## Results and Conclusion
The project includes comparative analyses of PLS and multivariate regression models for elements such as copper ('Cu'). While both models exhibit poor performance for copper, notable differences emerge in subsequent analyses, particularly for elements like manganese ('Mn'), where the multivariate regression model outperforms PLS in accurately predicting concentrations.

