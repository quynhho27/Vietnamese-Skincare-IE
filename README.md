## PROJECT OVERVIEW
The project focuses on Information Extraction (IE) using Natural Language Processing (NLP) techniques to extract structured information from Vietnamese skincare-related texts. 
The workflow includes manual data annotation with Label Studio, followed by Named Entity Recognition (NER) and Relation Extraction (RE) modeling.
Multiple models are implemented and compared using standard evaluation metrics to assess their effectiveness. 
The project demonstrates the practical applicability of NLP in supporting both consumers and businesses in the skincare domain.

## TASK FORMULATION

***1. Name Entity Recognition (NER)***
NER aims to identify and classify important entities appearing in Vietnamese skincare-related texts.
- Input: Vietnamese sentences
- Output: Token-level labels following the BIO tagging scheme
- Target entities: product ingredients, benefits, skin concerns, and origin information
- Model: CRF
- Results:
  + Accuracy: 88%
  + Precision: 78%
  + Recall: 76%
  + F1-score: 77%

***2. Relation Extraction (RE)***
Relation Extraction focuses on identifying semantic relationships between extracted entities.
- Input: Text containing annotated entity pairs
- Output: Relationship type between entities
- Vectorization: PhoBERT
- Models:
  + Machine Learning: SVM, Logistic Regression, Random Forest
  + Deep Learning: MLP
- Results:

| Metric | SVM | Random Forest | Logistic Regression | MLP |
|-------|-----|---------------|---------------------|-----|
| Accuracy | **0.89** | 0.79 | **0.87** | 0.84 |
| Near-Accuracy | **0.82** | 0.77 | **0.81** | 0.75 |
| Mid-Accuracy | **0.82** | 0.68 | **0.78** | 0.74 |
| Far-Accuracy | **0.98** | 0.87 | 0.96 | **0.97** |
| Macro F1-score | **0.89** | 0.76 | 0.85 | 0.80 |
| Weighted F1-score | **0.89** | 0.80 | **0.87** | 0.84 |
| Positive-only F1-score | **0.75** | 0.70 | **0.72** | 0.67 |

## TOOLS
- Programming Language: Python
- Database: MongoDB (for storing raw text and annotations for NER and RE)
- Data Annotation: Label Studio
- Libraries & Frameworks: PyTorch, scikit-learn, NLP utility libraries
- Experiment Tracking: MLFlow

> **Note**
> 
> This project was developed as a final course project in collaboration with three teammates
>
> This repository is a fork of the original group repository, in which I actively contributed to the core implementation and analysis

  
