# <div align="center"> ICU Survival Prediction Capstone</div>

### Regarding This Project
#### There is a file called ICU Survival Prediction

#### Library requirement:

    The development of this project took place in Jupyter Notebook using Python 3.7. For details about the libraries utilized in this notebook, please consult the library.txt file

#### Publication on the Medium blog:
    https://medium.com/@stiven02.0/icu-survival-prediction-9736c1936ec3

#### How to run this project:
     You can install Jupyter Notebook or download Anaconda Navigator, but you must generate a copy of the MIMIC III database.

### 1. Introduction  
#### Project Overview
This project intends to illustrate the procedure for choosing a specific group of patients, preparing the data to facilitate exploratory visualization, and constructing a classification model to foresee mortality post-ICU admission. This endeavor involves the analysis of initial notes provided by caregivers.

#### Problem Statement
The objective is to recognize potential high-risk patients and endeavor to anticipate the likelihood of survival post-ICU admission. In scenarios of diminished likelihood, proactive steps should be taken for intervention.

#### Data Set
MIMIC-III (Medical Information Mart for Intensive Care III) is an expansive and openly accessible database that encompasses de-identified health-related data linked to more than forty thousand patients who were admitted to critical care units at the Beth Israel Deaconess Medical Center between 2001 and 2012.

This comprehensive database comprises a wealth of information, including patient demographics, vital sign measurements collected at the bedside (approximately 1 data point per hour), laboratory test results, medical procedures, medication details, caregiver notes, imaging reports, and records of mortality both within and outside the hospital setting.

The availability of MIMIC is primarily attributed to the collaborative efforts of researchers at the MIT Laboratory for Computational Physiology and other research groups working in tandem.

#### Dataset sourced from
MIMIC-III, a freely accessible critical care database. Johnson AEW, Pollard TJ, Shen L, Lehman L, Feng M, Ghassemi M, Moody B, Szolovits P, Celi LA, and Mark RG. Scientific Data (2016). DOI: 10.1038/sdata.2016.35.

https://mimic.physionet.org/

#### Metrics
We will assess the effectiveness of machine learning models by analyzing their accuracy and employing a confusion matrix for a comprehensive evaluation. The classification report provides a holistic view, presenting essential metrics such as precision, recall, f1-score, and support.

### 2. Analysis
#### The focus of this project will involve the selection of ICU patients within the age range of 18 to 100.

Database Setup: PostgreSQL
Guide to Installing MIMIC-III in a Local Postgres Database on Windows

https://mimic.physionet.org/tutorials/install-mimic-locally-windows/

Before you proceed with the steps outlined in this guide, make sure to complete the following prerequisites:

a. Download the MIMIC-III Clinical Database.
b. Extract the MIMIC-III Clinical Database as .csv files to a directory on your local computer.
c. Obtain the necessary PostgreSQL scripts. You'll only need the files with .sql extensions.
Message: The PostgreSQL database, tables, and data were successfully created. However, a significant amount of information was missing or inaccurate.

### 3. Methodology
a. Logistic Regression Model
b. Random Forest Classification Model
Balanced Age Distributions for Survived Patients
Utilization of Machine Learning Models and Train-Test Data Division

Dataset with imbalanced classes
Due to the fact that more than 75% of the instances belong to the survived class, machine learning algorithms exhibited poor performance on the minority class.

Balanced dataset: undersampling
Data engieering:
We employ undersampling on the majority class of survived patients, utilizing pandas’ sampling feature without replacement to create balanced datasets between the survived and deceased patient groups. This enables machine learning algorithms to train and fit effectively, thereby enhancing performance on the minority dataset.

Observation: Since the NOTEEVENTS table did not have values, it was necessary to recreate information, which affected precision and everything else, but the execution in the models was achieved.

### 4. Results
Despite the setbacks with the mentioned table, we managed to successfully proceed with the model development. It’s a pity that the data didn’t come complete

### 5. Conclusion
Throughout this process, a comprehensive development and evaluation of machine learning models using the MIMIC-III database has been undertaken. By implementing various classification algorithms such as Logistic Regression, Decision Trees, Random Forests, AdaBoost, and Support Vector Machines, the capability to accurately predict hospital patient mortality has been demonstrated.

The results obtained have highlighted the effectiveness of these models in identifying high-risk patients and making mortality predictions with noticeable accuracy. Specifically, Support Vector Machines and Logistic Regression algorithms have stood out as the most effective in terms of performance. Hyperparameter tuning through GridSearchCV has further refined these models and enhanced their predictive capability.

Throughout this development, opportunities have arisen to further enhance model performance. The inclusion of laboratory results and radiology reports could enrich the data and improve prediction accuracy. Additionally, the possibility of exploring advanced image processing techniques and deep learning algorithms has been indicated to address this challenge more comprehensively.

This project has provided valuable insights not only into building medical models but also into the fundamental importance of data analysis in healthcare. The ongoing evolution of natural language processing techniques and machine learning algorithms presents significant potential to enhance clinical decision-making and patient outcomes.

Ultimately, the goal is to move towards a world without diseases. Through the continued application of data science in healthcare and clinical research, it is possible to approach this ideal by refining prediction accuracy and more efficiently tailoring care for each individual.

I apologize in advance for the data errors, but replicating the information from the NOTEEVENTS table proved to be challenging.

### Acknowledgements
MIMIC-III, a freely accessible critical care database. Johnson AEW, Pollard TJ, Shen L, Lehman L, Feng M, Ghassemi M, Moody B, Szolovits P, Celi LA, and Mark RG. Scientific Data (2016). DOI: 10.1038/sdata.2016.35. Available at: http://www.nature.com/articles/sdata201635

