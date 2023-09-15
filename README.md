# ChromSpec
This project explores using multivariate logistic regression for multi-label classification of unknown compounds using gas chromatography–mass spectrometry data and an in-house collected library which the logistic model was trained on.
Context of data collected:
1. 3 dimensional data (x, y, z) axes
2. Specific mass spectra (m/z) and total ion current (TIC) distribution at a specific retention time (RT) allows for identification of compound

Graphical illustration of the 3 dimensions of data collected can be seen below:
![image](https://github.com/nigelmaxwee/ChromSpec/assets/122780978/bf36fecf-ba03-4621-bbc5-8c8cfc55840e)


Main parts of the code include:
1. Preprocessing of data (data extraction from raw data files, normalisation within same scan number and one-hot encoding for classification of in-house library)
2. Feature engineering of data [time-bin encoding -> (35/0.25) time bins * 300 m/z = 42000 features per row per sample]
3. Modelling using logistic regression 

Features include:
1. Creating a new model from data
2. Using an existing trained model
3. Adding more data to existing models 

Disclaimer: In-house data was removed entirely and compound names replaced with arbitary names to ensure privacy of contents.

An example of the generated report can be seen below where each compound's models will give a probability of their respective compound existing in the sample:
![image](https://github.com/nigelmaxwee/ChromSpec/assets/122780978/53a676de-c4eb-4aa5-81c2-b4b76a594bab)
