# NLP Coursework

This repository contains my submission for the NLP coursework on detecting **patronising and condescending language (PCL)** in news text.

## Repository contents

* `BestModel/` – final submitted model, code/notebook, checkpoint, and instructions
* `notebooks/` – exploratory data analysis and development notebooks
* `figures/` – figures used in the report
* `dev.txt` – predictions for the official dev set
* `test.txt` – predictions for the official test set
* `data/` – coursework data files used during development

## Submitted approach

The final submitted system is a **RoBERTa-based classifier** trained for binary PCL detection with **class-weighted loss** to address label imbalance. Full details are given in the report and in `BestModel/README.md`.

## Reproducibility

To inspect or reproduce the submitted model, see:

* `BestModel/README.md`

This folder contains the final model, its training/inference code, and any configuration needed to reproduce the submitted predictions.

## Report

The written report is submitted separately as a PDF. The report includes:

* Exercise 1: critical paper review
* Exercise 2: exploratory data analysis
* Exercise 3: proposed approach
* Exercise 5.2: local evaluation
* Conclusion

## Notes

The official prediction files are provided at the top level of the repository so they are easy to find:

* `dev.txt`
* `test.txt`
