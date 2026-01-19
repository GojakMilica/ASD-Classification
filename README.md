# Adult Autism Classification — Machine Learning Evaluation Project

Educational machine learning project focused on **data preprocessing, feature analysis,
model comparison, and offline evaluation** using the Adult Autism Screening Dataset.

> This project is **not intended for clinical use**.  
> It is an academic course project aimed at analyzing and comparing different
machine learning approaches on a real-world dataset.

---

## Project Focus

The goal of this project was not to build a production medical system, but to:
- design and document a complete ML pipeline
- compare multiple classification approaches
- analyze feature relevance using statistical measures
- study the impact of model complexity and regularization on performance metrics

---

## Dataset

- **Source**: Adult Autism Screening Dataset (public)
- **Samples after preprocessing**: 696
- **Task**: Binary classification (ASD / NO ASD)
- **Label origin**: Derived from questionnaire scoring (not clinical diagnosis)

### Feature groups
- AQ-10 questionnaire scores (A1–A10)
- Demographic attributes
- Medical history indicators
- Relationship/context features

---

## Implemented Models

### k-Nearest Neighbors (kNN)
- Non-parametric baseline classifier
- Parameter selection performed by optimizing classification accuracy
- Achieves high specificity, with lower sensitivity depending on the choice of *k*

### Linear Discriminant Analysis + Gaussian Classifier
- Linear dimensionality reduction followed by probabilistic classification
- Computationally efficient and interpretable
- Exhibits high sensitivity with lower precision compared to other methods

### Neural Networks (PyTorch)
- Fully connected feed-forward architectures
- Multiple configurations explored:
  - underfitted networks
  - overfitted networks
  - regularized networks (dropout, L2 regularization, early stopping)
- Used to analyze:
  - the effect of model capacity
  - overfitting behavior
  - the impact of regularization techniques

---

## Evaluation Protocol

- Offline evaluation using:
  - accuracy
  - precision
  - recall (sensitivity)
  - specificity
  - F1 score
- All models evaluated under the same preprocessing pipeline
- Overfitting analyzed through training and validation loss behavior

> Reported results correspond to the evaluation protocol described in the report.
Minor variations may occur depending on model configuration.

---

## Key Takeaways

- The dataset exhibits a strong deterministic relationship between input features and labels,
  resulting from the way the ground truth is constructed.

- In this context, overfitting does not necessarily imply poor generalization, since the same
  underlying rule applies across the entire dataset.

- Differences between models are primarily reflected in the trade-off between sensitivity
  and specificity, rather than in their ability to learn the decision boundary.

- Simpler models such as LDA and kNN remain competitive, offering advantages in
  interpretability and computational efficiency.

- The main limitation of the project lies in the dataset itself: labels are derived from a
  screening questionnaire rather than clinical diagnosis, which limits real-world applicability.

---

## Academic Integrity

This repository documents a **course project**.
To avoid enabling copy-paste solutions for future students:
- The dataset is not included
- The repository focuses on documenting methodology and results rather than providing
  a fully runnable end-to-end solution

A detailed experimental report is provided for transparency.

---

## Report

📄 `ASD_Classification_Experimental_Report.pdf`

---

## Contributors

- **Milica Gojak**
- **Vladan Bašić**
