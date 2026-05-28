# Implementation Artifacts

## Purpose

This page summarizes the implementation artifacts associated with the proposed human-centered XAI pipeline.

The goal is to document the main computational components used to generate the technical artifacts, comparative results, and LLM-based XAI reports.

## Pipeline Implementation

The pipeline was organized into modular stages, including:

1. data ingestion;
2. exploratory data analysis;
3. preprocessing;
4. feature selection;
5. classification;
6. result assessment;
7. structured JSON artifact generation;
8. LLM-based report generation;
9. human-centered evaluation.

## Configuration

The implementation used external configuration files to support reproducibility and controlled experimentation.

Configuration files defined elements such as:

- dataset selection;
- feature-selection method;
- classifier type;
- cross-validation settings;
- metric calculation;
- output paths;
- LLM reporting settings.

## Structured Artifacts

The system generated structured JSON artifacts from the feature-selection and classification stages.

These artifacts summarized:

- dataset information;
- selected features;
- model configuration;
- classification metrics;
- feature-selection behavior;
- runtime information;
- metadata required for LLM-based reporting.

The JSON artifacts served as the intermediate representation between the technical layer and the LLM reporting layer.

## Reproducibility Notes

The experiments were designed to follow a reproducible workflow.

Key reproducibility elements included:

- modular pipeline stages;
- stratified 5-fold cross-validation;
- explicit data leakage control;
- structured outputs;
- fixed-prompt LLM reporting;
- separation between technical artifacts and human-readable reports.

## Data Privacy and Safety

No raw patient data were provided to the LLM.

The LLM received structured JSON artifacts derived from the technical stages of the pipeline.

The generated reports were not intended to provide diagnosis, treatment recommendations, or patient-level clinical decisions.

## Repository Status

This repository provides supplementary materials for the IEEE CBMS 2026 poster presentation.

Implementation materials may be progressively updated after the conference to include additional scripts, configuration examples, and archival artifacts.

A final archival version will be released later through Zenodo.
