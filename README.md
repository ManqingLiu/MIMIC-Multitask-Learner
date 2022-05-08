# MIMIC-Multitask-Learner

This project emulates an existing model by Kaji and team in their 2019 paper ["An
attention based deep learning model of clinical events in the intensive care
unit"](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0211057)
([repo](https://github.com/deepak-kaji/mimic-lstm)).


## Primary research question

Sepsis is responsible for over 5.3 million deaths annually and has an overall mortality rate of 30% in intensive care units [2]. The early identification and diagnosis of sepsis are critical for improving survival outcomes. As intensive-care clinicians are presented with large quantities of different measurements from multiple monitors in critical care units, machine learning models that can integrate data from multiple sources are crucial to predict mortality, sepsis risk, and myocardial infarction easily and quickly. These models could be the first step in building early-warning systems. This project aims to predict these three outcomes with multitask learning using long short-term memory (LSTM) recurrent neural networks (RNNs) to improve the predictions in the literature [3].

## Methods
LSTM RNNs will be used for the primary prediction tasks to account for sequential features in the MIMIC dataset. In comparison to previous implementations, a multitask learning approach will be used [3, 4]. Because each of the outcomes is a major adverse event in the ICU, multitask learning is expected to strengthen the models discriminatory ability through regularization and by learning rich, shared representations in the feature space. The final model will be compared to the previous LSTM approach with independent models for sepsis, MI and mortality along with logistic regression models that will serve as baseline comparators. Results will be reported using Accuracy, AUROC and AUPRC.

## Data
The Medical Information Mart for Intensive Care III (MIMIC-III) dataset will be used for this project. MIMIC-III is a freely-available, single-center database consisting of deidentified health data of more than 60,000 hospital admissions to critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012 [1]. The dataset consists of 26 data tables including information about all charted observations for patients, diagnoses, procedures done in units, laboratory tests performed and their results, intake of patients (e.g., intravenous medications, enteral feeding), outputs of patients, microbiology culture results, deidentified notes of ECG reports, radiology reports, and discharge summaries, and the admission and discharge dates of patients.

Since getting access to this dataset needs training and approvals from PhysioNet, dataset is not included in this repository. 

## References

1. Johnson, A., Pollard, T., Shen, L. et al. MIMIC-III, a freely accessible critical care database. Sci Data 3, 160035 (2016). https://doi.org/10.1038/sdata.2016.35.
2. Hou, N., Li, M., He, L. et al. Predicting 30-days mortality for MIMIC-III patients with sepsis-3: a machine learning approach using XGboost. J Transl Med 18, 462 (2020). https://doi.org/10.1186/s12967-020-02620-5.
3. Kaji, Deepak A., et al. An attention based deep learning model of clinical events in the intensive care unit. PloS one 14.2 (2019): e0211057.
4. Harutyunyan, H., Khachatrian, H., Kale, D.C. et al. Multitask learning and benchmarking with clinical time series data. Sci Data 6, 96 (2019). https://doi.org/10.1038/s41597-019-0103-9.

