# Comparative Results Summary

## Method Combinations

The experimental comparison evaluated four method combinations:

- Differential Evolution (DE) + Support Vector Machine (SVM)
- Differential Evolution (DE) + Random Forest (RF)
- Particle Swarm Optimization (PSO) + Support Vector Machine (SVM)
- Particle Swarm Optimization (PSO) + Random Forest (RF)

A baseline model without metaheuristic feature selection was also included for reference in the extended per-dataset tables.

## Poster-Level Summary

The poster reports a compact comparison focused on ROC-AUC, number of selected features, and runtime.

| Method | ROC-AUC | Selected Features | Runtime (s) |
|---|---:|---:|---:|
| DE + SVM | 0.990 | 10.8 | 14.730 |
| DE + RF | 0.987 | 11.0 | 574.771 |
| PSO + SVM | 0.995 | 14.8 | 14.116 |
| PSO + RF | 0.992 | 15.6 | 569.599 |

## Interpretation of Poster-Level Results

PSO + SVM achieved the highest ROC-AUC and the lowest runtime among the tested configurations.

However, DE + SVM provided a more compact solution, using fewer selected features while maintaining competitive ROC-AUC and low runtime.

This supports the interpretation of DE + SVM as a strong practical trade-off between predictive performance, compactness, and computational cost.

## Extended Classification Metrics

The following tables provide the extended metrics calculated for each dataset and method combination.

### Breast Cancer

| FS | Class | Features | F1 | Precision | Recall | ROC-AUC | Accuracy | Runtime (s) |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| DE | RF | 11.0 | 0.931 | 0.940 | 0.925 | 0.987 | 0.949 | 574.771 |
| DE | SVM | 10.8 | 0.944 | 0.963 | 0.926 | 0.990 | 0.960 | 14.704 |
| PSO | RF | 15.6 | 0.940 | 0.960 | 0.925 | 0.992 | 0.956 | 569.599 |
| PSO | SVM | 14.8 | 0.934 | 0.958 | 0.915 | 0.995 | 0.953 | 14.117 |
| Baseline | Baseline | 30.0 | 0.969 | 0.981 | 0.981 | 0.981 | 0.977 | 0.021 |

### Heart Attack / Cleveland

| FS | Class | Features | F1 | Precision | Recall | ROC-AUC | Accuracy | Runtime (s) |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| DE | RF | 7.0 | 0.754 | 0.751 | 0.759 | 0.851 | 0.771 | 544.892 |
| DE | SVM | 7.8 | 0.757 | 0.792 | 0.744 | 0.860 | 0.781 | 9.317 |
| PSO | RF | 6.8 | 0.751 | 0.779 | 0.729 | 0.868 | 0.781 | 536.113 |
| PSO | SVM | 6.2 | 0.764 | 0.795 | 0.737 | 0.857 | 0.791 | 9.685 |
| Baseline | Baseline | 13.0 | 0.805 | 0.845 | 0.773 | 0.892 | 0.828 | 0.015 |

### Diabetes

| FS | Class | Features | F1 | Precision | Recall | ROC-AUC | Accuracy | Runtime (s) |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| DE | RF | 8.4 | 0.966 | 0.983 | 0.950 | 0.992 | 0.960 | 530.099 |
| DE | SVM | 8.2 | 0.937 | 0.938 | 0.938 | 0.970 | 0.923 | 14.651 |
| PSO | RF | 9.0 | 0.963 | 0.975 | 0.953 | 0.988 | 0.956 | 533.727 |
| PSO | SVM | 8.2 | 0.934 | 0.944 | 0.925 | 0.966 | 0.919 | 14.275 |
| Baseline | Baseline | 15.0 | 0.973 | 0.978 | 0.969 | 0.993 | 0.967 | 0.020 |

## Notes on Metrics

- **Accuracy** measures the overall proportion of correct predictions.
- **Precision** measures how many predicted positive cases were actually positive.
- **Recall** measures how many actual positive cases were correctly identified.
- **F1-score** balances Precision and Recall.
- **ROC-AUC** summarizes the ability of the classifier to separate classes across different classification thresholds.
- **Selected Features** indicates the average number of features retained by the feature-selection method.
- **Runtime** reports the computational time for the corresponding method configuration.

## Scope of Interpretation

These results should be interpreted within the scope of the current initial validation using clinical tabular datasets.

The purpose of the extended results is to provide additional transparency beyond the compact poster table, particularly for metrics such as Precision and Recall, which are relevant in medical classification contexts.

The results support the analysis of the technical layer of the pipeline. They are not intended to provide patient-level diagnostic conclusions.
