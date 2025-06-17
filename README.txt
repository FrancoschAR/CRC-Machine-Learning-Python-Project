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
