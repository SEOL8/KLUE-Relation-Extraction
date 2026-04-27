# KLUE Relation Extraction

## Overview
- This notebook documents the entire process of designing, training, and comparing five models (M1–M4, M3+LS) using the KLUE RE (Relation Extraction) dataset, including error analysis and improvement experiments.

## Model Pipeline

![Model Pipeline](Model.png)

## Notebook Structure 
| Section | Content |
|---------|------|
| 0 | Settings / Constants / Evaluation Functions |
| 1 | EDA |
| 2 | Pre processing — Typed Entity Marker |
| 3 | M1 — klue/bert-base (Baseline) |
| 4 | M2 — klue/roberta-base + typed marker |
| 5 | M3 — klue/roberta-large + typed marker |
| 6 | M4 — EXAONE-3.5-2.4B few-shot + Criteria for Selecting an LLM |
| 7 | M1~M4, M3+LS Summary |
| 8 | Error Analysis |
| 9 | Optimization Experiment — Label Smoothing α=0.1 |
| 10 | Conclusion / Limitations / Next Steps |

## Evaluation Metrics (KLUE RE Official Metric)
- Micro F1: Based on the 29 classes excluding "no_relation(label 0)"
- AUPRC   : All 30 classes, based on softmax 

## Result (Micro F1, AUPRC)
![Micro F1, AUPRC](result.png)
