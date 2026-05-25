# Example LLM-Generated XAI Report

The following report is reproduced as originally generated and used in the human evaluation. It has not been edited after the evaluation.

This example illustrates the type of human-readable XAI report produced from structured JSON artifacts. Some expressions may require further calibration in future versions to avoid implying clinical validation, diagnostic reliability, or patient-safety guarantees.

---

## Original LLM-Generated Report Used in the Human Evaluation

### *System Purpose*

This artificial intelligence–based decision-support system is designed to assist healthcare professionals by classifying structured clinical records into two categories. The system processes structured patient information to generate computational outputs that may require further review. It does not provide diagnosis, treatment recommendations, or clinical decision-making. Its outputs are intended solely as computational support.

### *Data and Evaluation*

The system’s performance was evaluated using publicly available data from the Cleveland database. This dataset contains 13 clinical variables per patient. Performance was validated using rigorous statistical protocols to ensure consistent predictive capability on previously unseen patients.

### *Baseline System vs. Compact System*

To facilitate interpretability, the system automatically identifies the most relevant clinical indicators (such as age, troponin levels, and medical history) from a total of 13 available variables. The system demonstrated that it can predict the condition using only 9 key indicators while maintaining an accuracy level of 78%. This indicates that the system does not require excessive data to remain reliable, prioritizing the most critical information for condition assessment without compromising patient safety.

### *Stability-Based Feature Focus*

**Primary Variables** (Consistently Selected):

* Age (Patient age)
* Sex (Biological sex)
* Fasting glucose (Glucose > 120 mg/dL)
* Exercise-induced ST segment depression
* Coronary angiography (Number of major vessels colored by fluoroscopy)
* Thal (Cardiac perfusion defect)

**Context Variables** (Frequently Selected):

* cp (Chest pain type)
* chol (Serum cholesterol)
* slope (ST segment changes during exercise)

### *Operational Conclusions*

* Focuses attention on a reduced and stable set of variables, streamlining data review.
* Reduces cognitive load by minimizing unnecessary information.
* Enhances transparency by consistently identifying the elements on which the system relies.

### *Limitations*

Results are based on a public dataset and do not reflect clinical validity.
The system’s scope is limited to computational support and should not be used for clinical decision-making.
The results are intended to complement, not replace, professional validation.
Results are based on a public dataset and do not reflect clinical validity.
The system’s scope is limited to computational support and should not be used for clinical decision-making.
The results are intended to complement, not replace, professional validation.
