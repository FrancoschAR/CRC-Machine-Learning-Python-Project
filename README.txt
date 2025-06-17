Predicting metastatic potential of colorectal cancer (CRC) using miRNA expression profiles
Project Summary


This project investigates the potential of microRNA (miRNA) expression profiles to classify primary colorectal tumors based on their metastatic potential. Leveraging machine learning algorithms and biologically selected features, the model aims to distinguish tumors that have released metastatic cells (Stage III–IV) from those that have not (Stage I–II).


miRNAs are small, non-coding RNAs that play key roles in post-transcriptional gene regulation. Recent research links specific miRNAs to crucial cancer behaviors like epithelial-mesenchymal transition (EMT), invasiveness, and progression. With the declining cost of next-generation sequencing (NGS), miRNA profiling is poised to become a routine clinical tool. This project explores how computational modeling can translate transcriptomic data into actionable clinical insights.


Data Source:


Origin: Genomic Data Commons (GDC) — National Cancer Institute, NIH.


Data Type: miRNA-seq transcriptome profiles.


Target Variable: Pathological stage (I–II vs. III–IV).


Preprocessing:  miRNA selection based on literature-supported involvement in tumor 
progression, outlier handling (capping) and one-hot encoding of the target variable.


Models Used


The following machine learning models were implemented:


Primary  models:
1- Random Forest Classifier
2- XG Boost Classifier


Secondary models: 
3- Logistic Regression
4- Support Vector Machines
5- K-Nearest Neighbors 


All the models were evaluated using stratified cross-validation and hyperparameter optimization techniques.


Performance


Accuracy metrics are preliminary. Further improvements using clinical variables and larger sample sizes are under development.


Random Forest Accuracy: ~0.65


XGBoost Accuracy: ~0.60


Logistic Regression Accuracy: ~0.65


SVMs Accuracy: ~0.60


K-Nearest Neighbor Accuracy: ~0.60

This project set out to develop a machine learning model capable of predicting the metastatic potential of colorectal tumors—specifically distinguishing between pathological stages I–II (non-metastatic) and III–IV (metastatic)—based solely on miRNA expression profiles. The motivation lies in the growing evidence that specific miRNAs play critical roles in cancer progression, including the regulation of epithelial–mesenchymal transition (EMT), which is closely linked to metastasis.

To achieve this goal, the project followed a structured pipeline:

Data Collection:
Expression data of selected miRNAs related to tumor progression and EMT was retrieved from the NIH’s Genome Data Commons (GDC), using publicly available transcriptome profiles.

Data Wrangling:
The datasets were preprocessed to handle missing values and unified into a single, analysis-ready DataFrame. Additional miRNAs associated with E-cadherin deregulation were incorporated to enrich the feature space.

Exploratory Data Analysis (EDA):
Initial analyses helped uncover patterns, feature distributions, and potential outliers in both the original and newly added miRNA features.

Outlier Handling:
Several methods were implemented to improve data quality, including IQR-based filtering, Isolation Forest, DBSCAN, One-Class SVM, and capping-based transformations.

Model Development and Evaluation:

Baseline models (Logistic Regression, Support Vector Machines, and k-Nearest Neighbors) were trained using different outlier-handled datasets.

Feature selection and transformations were applied to improve classifier performance.

Hyperparameter tuning and cross-validation ensured better model generalization.

Ensemble models (Random Forest and XGBoost) were then implemented, leveraging their robustness and superior performance in complex classification tasks.

Despite the steps taken, model accuracy plateaued at moderate levels. This highlights a common limitation in relying solely on molecular features. For future improvement, incorporating clinical variables (e.g., tumor grade, lymph node involvement, patient demographics) alongside miRNA data is essential to build a more comprehensive and predictive model.

Final Thoughts:
Machine learning has enormous potential to enhance clinical decision-making by providing data-driven tools for early diagnosis, prognosis, and personalized treatment strategies. In this project, we explored how miRNA expression profiles, an increasingly accessible form of molecular data, could help predict cancer behavior in a non-invasive and scalable way.

This work is a scientific proof of concept, and future iterations should aim to combine multi-omics and clinical datasets to reach clinically actionable accuracy levels.

Disclaimer:

All data used in this project is publicly available through the National Cancer Institute’s Genome Data Commons (GDC) and was accessed solely for scientific and educational purposes. No personal or sensitive information was used or disclosed.


