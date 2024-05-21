# Alzheimer's Disease Dataset

This Alzheimer's disease dataset is used to classify Normal Cognition (CN) and Alzheimer's disease (AD) cases. 

## Datasets 
In this study, we used T1-weighted structural magnetic resonance imaging (3D-MRI) from three prominent datasets for Alzheimer's disease research: Alzheimer's Disease Neuroimaging Initiative (ADNI) \cite{ADNI}, Australian Imaging, Biomarker \& Lifestyle Flagship Study of Ageing (AIBL) \cite{AIBL}, and Open Access Series of Imaging Studies (OASIS) \cite{OASIS}. Subjects in these datasets have been characterized using the Clinical Dementia Rating (CDR) scale, where 0 indicates cognitively normal (CN), and values from 1 to 3 indicate different stages of Alzheimer's disease (AD) [Hughes_Berg_Danziger_Coben_Martin_1982](). Table \ref{table:dataset} shows the demographic information for these datasets.

<!--
## Datasets
T1-weighted structural magnetic resonance imaging (3D-MRI) images from three of the most popular datasets for detecting Alzheimer's Disease are used in this study: ADNI \cite{ADNI}, AIBL \cite{AIBL}, and OASIS \cite{OASIS}. In these datasets, subjects are characterized using the Clinical Dementia Rating (CDR) scale, which is a measure that ranges from 0 to 3 and is used to determine the overall severity of dementia. A CDR of zero characterizes CN cases, while a CDR of one or greater represents AD cases. Table \ref{table:dataset} shows the demographic information for these datasets.
-->

The datasets have been obtained from:

## ADNI
The Alzheimer's Disease Neuroimaging Initiative (ADNI) is a longitudinal multicenter study designed to develop clinical, imaging, genetic, and biochemical biomarkers for the early detection and tracking of Alzheimer's disease (AD) <a href="http://adni.loni.usc.edu" target="_blank">ADNI</a>.

## AIBL
The Australian Imaging, Biomarker \& Lifestyle Flagship Study of Ageing (AIBL) is a study to discover which biomarkers, cognitive characteristics, and health and lifestyle factors determine the subsequent development of symptomatic Alzheimer’s Disease (AD) [go][AIBL]([)](https://aibl.csiro.au){:target="_blank" rel="noopener"}. 

## OASIS
The Open Access Series of Imaging Studies (OASIS) is a project aimed at making neuroimaging datasets of the brain freely available to the scientific community. OASIS-3 is a longitudinal neuroimaging, clinical, cognitive, and biomarker dataset for normal aging and Alzheimer’s Disease [go][OASIS](http://www.oasis-brains.org){:target="_blank" rel="noopener"}.

## Merged Dataset
To mitigate the challenge of performance reduction of prediction models across diverse demographic groups, our study encompasses a varied range of study populations across different age groups (young and old people) by consolidating ADNI, AIBL, and OASIS datasets, resulting in a merged dataset of 420 instances. Each dataset contributes 70 volumes per class from each volume dataset (70 samples ${\times}$ 2 classes ${\times}$ 3 datasets).

| Dataset | Class | Subjects | Age | Gender | Total |
| --- | --- | --- | --- | --- | --- |
| | | | | F/M | Subjects |
| ADNI | CN | 70 | ${78.63 \pm 5.82}$ | 34/36 | 140 |
| | AD | 70 | ${78.63 \pm 6.50}$ | 31/39 | |
| AIBL | CN | 70 | ${74.56 \pm 5.81}$ | 37/33 | 140 |
| | AD | 70 | ${74.87 \pm 7.57}$ | 43/27 | |
| OASIS | CN | 70 | ${69.89 \pm 9.38}$ | 39/31 | 140 |
| | AD | 70 | ${76.36 \pm 9.15}$ | 34/36 | |
| Merged | CN | 210 | ${74.36 \pm 8.01}$ | 110/100 | 420 |
| | AD | 210 | ${76.62 \pm 7.93}$ | 108/102 | |

## Volume Dataset Building.
Volumes per subject are sorted by visit date, with only the last visit included in the dataset to ensure one volume per subject. 
The datasets are then randomly split to ensure reproducible tests and prevent data leakage. Each MRI volume per subject is exclusively included in one distribution (train, validation, or test). 
The subject dataset is split between training (70\%), validation (15\%), and test (15\%) sets. 
The subject distribution is balanced, with the same number of subjects per class ($k$), where $k$ is less than or equal to the number of samples from the minority class, addressing class imbalance issues.

## Volume Datasets

| Dataset | Train | Validation | Test |
| --- | --- | --- | --- |
| ADNI | [Train](adni_train_volumes.csv) | [Validation](adni_validation_volumes.csv) | [Test](adni_test_volumes.csv) |
| AIBL | [Train](aibl_train_volumes.csv) | [Validation](aibl_validation_volumes.csv) | [Test](aibl_test_volumes.csv) |
| OASIS | [Train](oasis_train_volumes.csv) | [Validation](oasis_validation_volumes.csv) | [Test](oasis_test_volumes.csv) |
| Merged | [Train](train_volumes.csv) | [Validation](validation_volumes.csv) | [Test](test_volumes.csv) |

## File content
Each CSV dataset file contains these columns: 

| # | Name | Description |
| --- | --- | --- |
| 1 | index | The consecutive number. |
| 2 | group | The corresponding dataset repository (ADNI, AIBL, or OASIS). |
| 3 | subject | The subject ID assigned by the dataset repository. |
| 4 | sex | The genre (F=Female, M=Male). |
| 5 | age | The patient's age at the scan test. |
| 8 | visit | The number of the visit. |
| 7 | image_data_id | The image ID assigned by the dataset repository. |
| 8 | acq_date | The MRI scan acquisition date. |
| 9 | cdr | The Clinical Dementia Rating (CDR). |
| 10 | MMSE | The Mini-mental State Exam score. |
| 11 | filename | The MRI filename as downloaded from the repository. |
| 12 | class | The label class (CN=Conitive Normal, AD=Alzheimer's Disease) |


<!--
- ADNI
  - [Train](adni_train_volumes.csv)
  - [Validation](adni_validation_volumes.csv)
  - [Test](adni_test_volumes.csv)
- AIBL
  - [Train](aibl_train_volumes.csv)
  - [Validation](aibl_validation_volumes.csv)
  - [Test](aibl_test_volumes.csv)
- OASIS
  - [Train](oasis_train_volumes.csv)
  - [Validation](oasis_validation_volumes.csv)
  - [Test](oasis_test_volumes.csv)


## Distribution datasets

- [Train](train_volumes.csv)
- [Validation](validation_volumes.csv)
- [Test](test_volumes.csv)
 
[a relative link](other_file.md)
-->












