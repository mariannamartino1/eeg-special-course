# Resting-state EEG Analysis for Diagnostic Purposes - Code

This repository contains the code used to analyze eyes-open (EO) and eyes-closed (EC) resting-state EEG recordings.

## Data source

The EEG data come from the **Dortmund Vital Study resting-state EEG dataset**:

Getzmann et al. (2024), *Scientific Data*  
https://www.nature.com/articles/s41597-024-03797-w

The raw data are not included in this repository.

## Repository structure

- `scripts/` contains the cleaned notebooks used for the final analysis.
  - `00` / `01`: manifest construction and dataset inspection.
  - `02` / `02b`: preprocessing, Welch features, and FOOOF/specparam features.
  - `03a` / `03b` / `03c`: paired, subject-independent, and epoch-calibrated classification analyses.

- `data_processed/` contains derived CSV files, including feature tables and model results.

- `figures/` contains output figures used for inspection and the final report.

- `old/` contains earlier exploratory and messy analyses that were later cleaned and reorganized into the `scripts/` folder.

## Main question

The analysis compares a simple posterior-alpha baseline with more complex EEG spectral classifiers, while testing how performance changes between paired, subject-independent, and participant-calibrated prediction settings.
