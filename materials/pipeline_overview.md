# Pipeline Overview

The proposed pipeline provides system-level explainability for embedded AI in medical equipment.

It is designed to translate the internal behavior of an AI-based classification component into accessible XAI reports for healthcare professionals and clinical decision makers.

## Pipeline Stages

1. **Clinical Dataset**  
   Tabular clinical data used for initial validation.

2. **Technical Specifications**  
   Technical information relevant to AI-enabled medical equipment.

3. **Exploratory Data Analysis**  
   Data understanding, distributions, correlations, missing values, and outliers.

4. **Feature Selection**  
   Differential Evolution (DE) and Particle Swarm Optimization (PSO) are used to identify compact feature subsets.

5. **Classifier**  
   Support Vector Machine (SVM) and Random Forest (RF) are trained using the selected features.

6. **Result Assessment**  
   Model results are checked using classification metrics and validation criteria.

7. **Structured Artifacts**  
   The system generates structured JSON outputs describing metrics, selected features, and model behavior.

8. **LLM Reporting**  
   A fixed prompt is used to generate a human-readable XAI report from the structured artifacts.

9. **XAI Report**  
   The report summarizes system-level behavior in accessible language.

10. **Human Evaluation**  
   Healthcare professionals evaluate the clarity, coherence, and usefulness of the generated explanations.

## Scope

The pipeline does not provide patient-level diagnosis, treatment recommendations, or clinical decision-making.

Its purpose is to support transparent understanding and evaluation of embedded AI behavior.
