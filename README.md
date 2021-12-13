# A Bayesian Latent Vector Model Approach to Cognitive Decline Prediction via fMRI Imaging
We propose a Bayesian approach to predicting the brain age of a patient through brain imaging scans as a function of the latent vector space and conditional probabilities derived from demographic characteristics.

# Data
The dataset utilized are the 600 functional MRI scans collected by the IXI Brain Study conducted by Imperial College London over a period between 2005 and 2006. The study included 3 study sites (Hammersmith Hospital, Guy’s Hospital, Institute of Psychiatry)  with varying machine specifications (Philips 3T system, Philips 1.5T system, GE 1.5T system respectively). All patients were healthy at the time of the scan. Each scan was archived in both T1 and T2 weighted formats and also included demographic information for each patient. 

Demographic information collected included occupational status, occupational field, marital status, highest educational levels, and even standardized testing results.

Of the 600 scans available, 509 were ultimately determined to have valid demographic and scan information. Exclusion reasons include high outliers in height or weight and unreasonable or missing ages features among others.

# Method
The file (```fMRI_EDA.ipynb```) will download the IXI data and illustrate how the 3-dimensional image space can be sampled from in different perspectives. It also illustrates the distribution of pixel intensities from the dataset. To run the model, first run (```PCA.ipynb```) to generate a reduced dimensionality input of the latent vector space. The Bayesian method itself is found in (```bayesianRegression.ipynb```), which requires the output of (```PCA.ipynb```) and the demographic data found in the (```/Data```) folder.

The final trained torch model as well as the latent vector representations can also be found in the (```/Data```) folder.
