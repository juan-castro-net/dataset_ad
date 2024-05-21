# Alzheimer's Disease Dataset

This Alzheimer's disease dataset is used to classify Bornal Cognitio (CN) and Alzheimer's disease (AD) cases. 

## Groups
- OASIS
- ADNI
- AIBL

## Columns
Each csv file have these columns: 
1. index
2. group
3. subject
4. sex
5. age
6. visit
7. image_data_id
8. acq_date
9. cdr
10. mmse
11. filename
12- class

## Datasets 
In this study, we used T1-weighted structural magnetic resonance imaging (3D-MRI) from three prominent datasets for Alzheimer's disease research: Alzheimer's Disease Neuroimaging Initiative (ADNI) \cite{ADNI}, Australian Imaging, Biomarker \& Lifestyle Flagship Study of Ageing (AIBL) \cite{AIBL}, and Open Access Series of Imaging Studies (OASIS) \cite{OASIS}. Subjects in these datasets have been characterized using the Clinical Dementia Rating (CDR) scale, where 0 indicates cognitively normal (CN), and values from 1 to 3 indicate different stages of Alzheimer's disease (AD) \cite{Hughes_Berg_Danziger_Coben_Martin_1982}. Table \ref{table:dataset} shows the demographic information for these datasets.

## Merged Dataset
To mitigate the challenge of performance reduction of prediction models across diverse demographic groups, our study encompasses a varied range of study populations across different age groups (young and old people) by consolidating ADNI, AIBL, and OASIS datasets, resulting in a merged dataset of 420 instances. Each dataset contributes 70 volumes per class from each volume dataset (70 samples ${\times}$ 2 classes ${\times}$ 3 datasets).

| Dataset | Class | Subjects | Age | Gender | Total |
| --- | --- | --- | --- | --- | --- |
| | | | F / M | Subjects |
| ADNI \cite{ADNI} | CN | 70 | ${78.63 \pm 5.82}$ | 34/36 | 140 |
| | AD | 70 | ${78.63 \pm 6.50}$ | 31/39 | |
| AIBL \cite{AIBL} | CN | 70 | ${74.56 \pm 5.81}$ | 37/33 | 140 |
| | AD | 70 | ${74.87 \pm 7.57}$ | 43/27 | |
| OASIS \cite{OASIS} | CN | 70 | ${69.89 \pm 9.38}$ | 39/31 | 140 |
| | AD | 70 | ${76.36 \pm 9.15}$ | 34/36 | |
| --- | --- | --- | --- | --- | --- |
| Merged | CN | 210 | ${74.36 \pm 8.01}$ | 110/100 | 420 |
| | AD | 210 | ${76.62 \pm 7.93}$ | 108/102 | |






