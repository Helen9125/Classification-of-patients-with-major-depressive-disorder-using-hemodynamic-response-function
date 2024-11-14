# Classification-of-patients-with-major-depressive-disorder-using-hemodynamic-response-function

## Introduction
Major depressive disorder (MDD) is a severe affective disease with high morbidity. Patients with MDD often have suicidal ideation (SI), and MDD is associated with approximately 31 % of lifelong suicide attempts (SA). Several research have revealed the correlation with brain region and the occurence of MDD. However previous studies mostly focused on a single subgroup (SA or SI), moreover, traditional statistics can only report group level-differences while individual level-differences are necessary to improve clinical application.

## Aim
We aim to investigate the potential of using HRF parameters to distinguish patients with major depressive disorder and different severities of suicidal intention.

## Methods
* Subjects
  - We will use retrospective data from previous clinical trials from Taipei Veterans General Hospital.
  - Total 302 subjects, consisting of MDD patients with different severity of suicidal intention and healthy controls.
  - Imaging data including T1-weighted images and Resting state fMRI are used.
* Feature Extraction
  - Automated Anatomical Labeling (AAL), which typically used in functional neuroimaging-based research to obtain neuroanatomical labels, is ultilized for feature selection.
  - Since depression may correlate with certain brain change, this experiment only used the first 90 regions in AAL as features.
* Methods for Feature Selection
  - Without feature selection: Using all features for model training.
  - Correlation – depression versus healthy group: Selecting features that has strong correlations with the depression diagnosis (p < 0.05).
  - Correlation – MADRS: Selecting features that has strong correlations with MADRS score (p < 0.05).
  - Logistic regression: Utilizing a logistic regression model to identify features that significantly contribute to depression classification.
* Models for Classification
  - Support vector machine (SVM)
  - Random forest (RF)
  - Logistic regression
  - K-Nearest neighbors (KNN)
* Evaluation Metrices
  - Accuracy
  - Precision
  - Recall
  - F1 score
## Results
Regression model outperformed other models with the accuracy of 71% and 0.86 on F1-score.
![image](https://github.com/user-attachments/assets/efcea442-d115-43ea-9324-ac56b5a8d914)

## Conclusion
* Several brain regions show to have higher correlation to MDD, these regions including frontal, limbic, occipital, parietal, sub-cortical.
* Previous research has found the association between frontal area as well as cingulate cortex and major depressive disorder, which fits with our findings.

## Limitations and Potential Solutions
* The classification performance in our study is not great, we speculate this might be due to that we have rather small sample size, especially for healthy controls.
* We haven’t try data augmentation yet, which might help mitigate the influence of data imbalance issue.
* The unit for HRF RH is percentage change in signal, while the unit for HRF TTP and FWHM is seconds, standardizing the parameters might help improve the performance of the model.




