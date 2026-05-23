# Extended Methodological Notes

## Scope of the Work

This work presents a human-centered explainable AI (XAI) pipeline for embedded AI in medical equipment, with an initial validation using clinical tabular datasets.

The purpose of the pipeline is not to provide patient-level diagnosis or replace clinical judgment. Instead, it supports a more transparent understanding of how an AI-based classification component behaves internally.

## Pipeline Overview

The pipeline starts from clinical tabular data and technical specifications relevant to AI-enabled medical equipment.

It then moves through:

- exploratory data analysis;
- metaheuristic feature selection;
- supervised classification;
- structured artifact generation;
- fixed-prompt LLM reporting;
- human-centered evaluation.

## Technical Layer

At the technical level, the pipeline analyzes the internal behavior of the embedded AI component in terms of:

- predictive performance;
- feature compactness;
- computational cost;
- feature-selection behavior across datasets.

The tested configurations combined:

- Differential Evolution (DE);
- Particle Swarm Optimization (PSO);
- Support Vector Machine (SVM);
- Random Forest (RF).

## Human-Centered Layer

The technical outputs are organized into structured artifacts. These artifacts are used by the LLM to generate human-readable XAI reports.

The generated reports are intended to help healthcare professionals and clinical decision makers better understand how the embedded AI component behaves internally.

## Safeguards

The pipeline was designed with the following safeguards:

- no raw patient data are provided to the LLM;
- the LLM receives structured artifacts derived from the evaluation pipeline;
- fixed prompts are used to reduce uncontrolled variation;
- the reports are not intended to provide diagnosis or clinical recommendations.

## Evaluation

The initial validation used clinical tabular datasets and compared different combinations of feature selection and classification methods.

The human-centered evaluation was conducted with healthcare professionals using a questionnaire adapted from the System Causability Scale.

## Limitations

The current evaluation should be understood as an initial validation.

Important limitations include:

- use of benchmark clinical tabular datasets;
- limited number of healthcare professionals in the human evaluation;
- no direct evaluation on real-world medical equipment scenarios;
- no exhaustive comparison with established XAI baselines such as SHAP or LIME;
- no systematic prompt robustness analysis.

## Future Work

Future work includes broader datasets, expanded technical configurations, real-world medical equipment scenarios, and richer human evaluation.
