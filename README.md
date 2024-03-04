# Emergency Department Patient Segmentation <br>Using Unsupervised Machine Learning Techniques  
WGU - BS Data Analytics Capstone Project  
Amanda Hanway - 3/2/2024  

## Introduction   
Visits to the Emergency Department (ED) generate costly bills for both the patient and their healthcare payer. In many cases, steps can be taken to prevent a potential medical emergency, such as taking prescribed medications and regularly seeing a Primary Care Provider for checkups.  
 
This project will focus on identifying patterns among individuals who visited the ED. Armed with this insight, the healthcare payer can take pre-emptive action to prevent emergency encounters as a cost-savings measure.  

## Links  
- Python Code: [View Capstone.ipynb](Capstone.ipynb)  
- Data Files: [View Data](data)  
  - The data for this project was provided by Synthea, an open-source, synthetic patient generator. The datasets mimic Electronic Health Records (EHR) to provide realistic (but not real) medical history for synthetic patients, enabling Health IT research and development. Source: https://synthetichealth.github.io/synthea/  
- Written Report: [tbd](tbd)  

### Research Question or Organizational Need
This project addressed the research question, “What shared characteristics are present among patients with emergency encounters?” This question was brought about by the organizational need for healthcare payers to identify individuals with a higher propensity to experience an emergency encounter. Armed with this insight, the healthcare payer can take pre-emptive action to prevent the encounter as a cost-savings measure. 
  
### Overview of Data Analytics Solution
The data analytics solution included the use of Exploratory Data Analysis (EDA), Principal Component Analysis (PCA), Unsupervised Machine Learning, and aspects of project management. The python programming language and python libraries such as pandas, numpy, matplotlib, sklearn, and seaborn were used within a JupyterLab environment to conduct analysis and develop the model.  

EDA was first conducted on a dataset of synthesized Electronic Health Records to understand its characteristics and identify underlying issues. Following the data cleaning and feature engineering steps identified through EDA, PCA was applied to the data to investigate and select important features. The data was then trained using the K-Means Clustering model. The initial model was developed, then tuned in iterations using the Agile project management methodology. The final model was applied to a second, unseen dataset, and the results were evaluated.  

### Data Selection and Collection
The data was downloaded from the Synthea website (SyntheticHealth, 2024) in two zipped folders which contained 16-18 files each. After reviewing the files individually in Excel, the five following files were chosen for further use in the model: 
1.	allergies.csv
2.	careplans.csv
3.	conditions.csv
4.	encounters.csv
5.	patients.csv

### Exploratory Data Analysis

### Data Cleaning & Feature Engineering
- Removed patients who did not have an emergency encounter
- Summarized counts of each encounter class per patient
- Summarized conditions per patient
- Created a column for patient age
- Identified and removed outliers for patient age
- Created patient age numerical categories
- Created healthcare expense numerical categories
- Created gender numerical categories
- Created race numerical categories
- Created county numerical categories
- Created a careplan indicator
- Created allergy one-hot encoded columns
- Joined datasets together into one main dataset
- Assessed and handled missing data
- Identified and removed outliers for emergency encounters

### Principal Component Analysis

### K-Means Model


### Conclusions
The largest cluster was Cluster 0 with 677 patients, followed by Cluster 1 with 71 patients and Cluster 2 with 52.

As shown in the bar charts above, the following prominant columns were identified for each cluster:

- Cluster 0 is driven by lack of or minimal presence of allergies, Hypertriglyceridemia disorder, Metabolic syndrome X, Suspected lung cancer or Carcinoma in situ of prostate.
- Cluster 1 is driven by presence of allergies.
- Cluster 2 is driven by presence of Hypertriglyceridemia disorder or Metabolic syndrome X.
  
### Limitations
A limitation of the model and analysis was the dataset. Given that the data was synthetic, it may not truly represent patterns in patients who have emergency encounters. Additionally, it is unknown if the 2020 and 2021 datasets were comprised of the same patients or a different group of patients.

### Future Work
An area for future work to improve the model is to develop condition groupers where each condition is assigned to a category made up of other similar conditions. The assumption is that this method would create more, smaller clusters, which would be made up of patients that share more-similar characteristics than the current method where each condition is treated separately.










<br>
<br>
<br>
<br>
<br>
<br>
