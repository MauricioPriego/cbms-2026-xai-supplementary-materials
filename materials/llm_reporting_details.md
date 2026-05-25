# LLM Reporting Details

## Purpose of the LLM Reporting Layer

The LLM reporting layer was designed to translate structured technical artifacts into human-readable XAI reports.

The goal was not to generate diagnoses, clinical recommendations, or patient-level explanations. Instead, the LLM was used to produce accessible summaries of the internal behavior of an AI-based classification component.

This layer supports the communication of system-level behavior to healthcare professionals and clinical decision makers.

## Input to the LLM

The LLM received structured JSON artifacts automatically generated from the feature-selection and classification stages of the proposed pipeline, summarizing information such as:

- model performance metrics;
- selected features;
- feature-selection behavior;
- method configuration;
- dataset-level behavior;
- explanatory metadata derived from the technical pipeline.

The JSON artifacts served as an intermediate representation between the technical layer and the LLM reporting layer.

This design helped keep the reporting process structured, reproducible, and focused on system-level behavior rather than raw patient data.

## Data Safeguards

No raw patient data were provided to the LLM.

The LLM did not receive individual patient records, direct clinical cases, or identifiable health information.

Instead, the input consisted of structured summaries derived from the evaluation pipeline.

This design was intended to reduce privacy risk and keep the LLM reporting layer focused on system-level explanation, rather than patient-level inference, diagnosis, or clinical recommendation.

## Fixed-Prompt Reporting Strategy

Several prompt formulations were explored during development before selecting a fixed prompt for the final reporting workflow.

The selected prompt was kept fixed across report generation to maintain consistency in tone, structure, and safeguards.

The fixed prompt used for the final reporting workflow is available here: [Fixed Prompt for LLM-Based XAI Report Generation](fixed_prompt_llm_reporting.md).

The prompt instructed the LLM to:

- summarize system-level behavior;
- avoid diagnostic recommendations;
- avoid patient-specific conclusions;
- describe selected variables and model behavior in accessible language;
- maintain a cautious and explanatory tone;
- distinguish technical evidence from clinical interpretation.

## Reporting Output

The output of the LLM was a human-readable XAI report.

The report was intended to help healthcare professionals understand:

- which variables were prioritized by the system;
- how the model behaved across the evaluated datasets;
- whether the selected feature subsets appeared compact or heterogeneous;
- how the technical behavior of the system could be interpreted at a system level.

The generated report was not intended to replace expert clinical judgment.

## LLM Model Exploration

During development, different Gemini model versions were explored for the reporting layer.

The same general reporting objective was maintained: transforming structured technical artifacts into accessible XAI reports.

| LLM Variant | Role in Development | Notes |
|---|---|---|
| Gemini variant 1 | Exploratory generation | Used to evaluate report clarity and structure. |
| Gemini variant 2 | Exploratory generation | Used to compare consistency and readability. |
| Final selected Gemini version | Reporting layer | Used for generating the reports evaluated in the study. |

The comparison between LLM variants was exploratory and was not designed as a full prompt-robustness or model-robustness study.

## Human Evaluation of Reports

The generated reports were evaluated by healthcare professionals.

The questionnaire was adapted from the System Causability Scale (SCS), an established framework for evaluating explanation quality.

The evaluation focused on perceived qualities of the generated explanations, including:

- completeness;
- interpretability;
- internal consistency;
- usability;
- usefulness for understanding the system.

The evaluation did not assess diagnostic correctness, because the pipeline was not designed to generate patient-level diagnoses.

## Limitations of the LLM Reporting Layer

The current LLM reporting layer has several limitations:

- the comparison between LLM variants was exploratory;
- prompt robustness was not systematically evaluated;
- the reports were generated from structured artifacts derived from benchmark clinical tabular datasets;
- the human evaluation involved a limited number of healthcare professionals;
- locally deployed LLMs were not evaluated in the current version.

## Future Work

Future work will explore:

- additional LLMs, including locally deployed models;
- systematic prompt-robustness analysis;
- broader technical configurations;
- richer human evaluation;
- real-world medical equipment scenarios;
- more detailed analysis of potential LLM limitations, biases, and failure cases.

## Summary

The LLM reporting layer serves as a translation mechanism between technical system behavior and human-centered explanation.

It does not replace clinical judgment and does not produce patient-level recommendations.

Its role is to transform structured technical artifacts into accessible XAI reports that can support more informed evaluation of embedded AI in medical equipment.
