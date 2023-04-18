# AutomaticEyeDiseasePrediction
In this project we are going to make use of Pupillometry device data to detect the eye diseases in Pediatric ages acqired through heriditary. Pupillometry device data is used, as this device is very accurate and it’s not require huge number of clinical test to detect disease. All existing techniques require huge number of clinical test to diagnose eye pupil disease in children’s and it’s not good for children’s health, so using Pupillometry device which capture pupil diameters continuously and records that data in raw format in the file. Later we can analyse that data using Machine Learning SVM algorithm to detect presence of disease. Here we use two different SVM classifiers to train right and left eye pupil data and then performing OR operations between two classifier using ENSEMBLE VOTING classifier to get classifier with better accuracy. SVM will assign disease class label as 1 to train data if pupils size diameter is huge and if its size is normal then classifier will assign value 0.

To implement this data author using Pupillometry raw data and perform below functions to diagnose pupils disease.

Upload Pupillometry Data: Using this module we will upload raw data which contains continuous recording of pupils data.

Filtering: Raw data contains huge number of buggy values and we will filter that raw data to extract only useful information such as pupil min and max diameter

Features Extraction: Using this module all pupil min and max features extracted from raw data.

Features Reduction: Using this module we will remove unnecessary features from raw data such as camera name, position etc to reduce features set. In this module we will extract features such as Patient ID, MAX, MIN, DELTA, CH etc. Extracted data can be used to split into train and test data

Right SVM: Using this module we will train SVM with right pupil data

Left SVM: using this module we will train SVM with left Pupil data and then apply SVM on test data to calculate prediction accuracy, sensitivity and specificity.

Ensemble Algorithm (Left & Right SVM): Using this module we will combine both classifier to get classifier with high prediction accuracy.

Predict Disease: using this module we will upload test data and then apply SVM classifier to predict disease.
