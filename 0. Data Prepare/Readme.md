# Prediction of Cell Health Phenotypes using Image-Based Morphology Profiling

## Overview
This repository contains resources and code related to the IDR-0080 project, focusing on predicting cell health phenotypes from Cell Painting assay data using machine learning techniques.

### Date
June 18, 2024

## Contents

1. [Proposal](#proposal)
2. [IDR 0080](#idr-0080)
3. [Open Source Database CPG-0012](#open-source-database-cpg-0012)
4. [Chemical Information Reference (Drug Repurposing Hub)](#chemical-information-reference-drug-repurposing-hub)
5. [Instructions for Use](#instructions-for-use)
6. [References](#references)

## Proposal

### Introduction
The aim of computational biology research is to efficiently analyze complex and vast amounts of biological data, discover new biological insights, drugs, and study diseases.

### Reason for Selecting Cell Image Data
Cell image data allows for the analysis of morphological features using artificial intelligence and machine learning, revealing previously incomprehensible biological insights.

### Types of Biological Data
- Genetic and Genomic Data
- Protein Data
- Metabolite Data
- Cell and Tissue Image Data
- Genetic Variation Data
- Physiological and Phenotypic Data
- Bioinformatics Data
- Ecological and Environmental Data
- Time Series Data

### What is Cell Painting?
Cell Painting is a high-content, multiplexed image-based assay used for cytological profiling, employing six fluorescent dyes to label different cellular components.

### General Workflow for Cell Painting Assay
1. Plate cells into labware (384-well plate)
2. Treat cells with chemical or genetic perturbations
3. Stain cells with fluorescent dyes
4. Acquire cell images with a high-content imaging system
5. Analyze cell images using automated image analysis software
6. Derive morphological profiles from measurements

### Limitations of Cell Image Dataset Formation
- High-Resolution Imaging Requirements
- Time-Consuming Image Acquisition
- Automation Limitations
- Data Volume
- Data Standardization
- Annotation and Labeling

## IDR 0080

### Title of Paper
Prediction of cell health phenotypes using image-based morphology profiling

### Summary
This paper develops a machine learning solution to predict cell health readouts directly from Cell Painting assay data.

### IDR-0080’s Flowchart
1. Retrieve single-cell profiles archived on Figshare
2. Generate and process Cell Painting and cell health assay readouts
3. Train regression models using Cell Painting data to predict cell health assay readouts
4. Apply trained models to Drug Repurposing Hub data for predicting drug perturbation effects
5. Use orthogonal readouts to validate predictions
6. Assess model robustness using sample size, feature groups, and cell line holdouts

### Data Sources
- [Cell Painting Data](https://idr.openmicroscopy.org/)
- [SQLite file (single cell profiles)](https://doi.org/10.35092/yhjc.9995672)
- [Drug Repurposing Hub Data](https://doi.org/10.5281/zenodo.3928744)

### Machine Learning Approach
- General Z-score Elastic Net regression model
- Split data into 85% training and 15% test sets
- Normalize data using EMPTY controls in each plate
- Optimize hyperparameters using 5-fold cross-validation
- Train models to predict 70 cell health assay readouts

### Full Model Accuracy Comparison
- [Figure 1: R^2 (Test) vs. R^2 (Train)](link_to_figure1)
- [Figure 2: Targets vs. R^2 (Test)](link_to_figure2)

## Open Source Database CPG-0012

### Description
This dataset comprises 919,265 five-channel fields of view, representing cellular responses to 30,616 compounds, with morphological features extracted at both individual and population levels.

### Reference Paper
[Application of Cell Painting for chemical hazard evaluation in support of screening-level chemical assessments, Toxicol Appl Pharmacol. 2023](link_to_paper)

### File Composition
- Image curation statistics (Metadata)
- Chemical annotation (Metadata)
- Pipeline (Metadata)
- Plate files (Mean well profiles, QC)

## Chemical Information Reference (Drug Repurposing Hub)

### Chemical Information
- [Drug Information](link_to_drug_info)
- [Sample Information](link_to_sample_info)

## Instructions for Use

### Clone the repository
```bash
git clone https://github.com/your/repository.git
cd repository
