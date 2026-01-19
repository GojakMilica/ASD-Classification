# Adult Autism Classification — Machine Learning Evaluation Project

Educational machine learning project focused on **data preprocessing, signal/feature ranking,
model comparison, and offline evaluation** using the Adult Autism Screening Dataset.

> This project is **not intended for clinical use**.  
> It is an academic project designed to study ML evaluation and trade-offs on a real-world dataset.

---

## Project Focus

The goal of this project was not to build a production medical system, but to:
- design a clean ML pipeline
- compare multiple modeling approaches
- analyze **feature relevance**
- reason about **metric trade-offs** (precision vs recall vs specificity)


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
- Used as a strong non-parametric baseline
- High interpretability
- Strong specificity, useful when false positives are costly

### Linear Discriminant Analysis + Gaussian Classifier
- Dimensionality reduction + probabilistic modeling
- Efficient and interpretable baseline
- Useful when compute or latency is constrained

### Neural Networks (PyTorch)
- Multiple architectures explored:
  - underfitted
  - overfitted
  - regularized (dropout, L2, early stopping)
- Used to study:
  - capacity vs generalization
  - regularization effects
  - early stopping as an implicit ranking constraint

---

## Evaluation Protocol

- Offline evaluation using:
  - accuracy
  - precision
  - recall (sensitivity)
  - specificity
  - F1 score
- Models compared under the same preprocessing pipeline
- Overfitting analyzed via training/validation behavior

> Results vary slightly depending on split and regularization strategy.  
> Full experimental details are provided in the report.

---

## Key Takeaways

- The dataset exhibits a strong, deterministic relationship between input features and labels,
  making the classification task highly separable.

- In this setting, overfitting does not necessarily indicate poor generalization, as the same
  underlying rule applies across the entire dataset.

- Different models primarily differ in the balance between sensitivity and specificity,
  rather than their ability to learn the decision boundary.

- Simpler models (LDA, kNN) remain competitive and offer advantages in interpretability
  and computational efficiency.

- The main limitation of the project is the dataset itself: labels are derived from a screening
  questionnaire rather than clinical diagnosis, limiting real-world applicability.

---

## Academic Integrity

This repository documents a **course project**.
To avoid enabling copy-paste solutions for future students:
- The dataset is not included
- The repository documents the project and its results, rather than providing a ready-to-run solution.


A detailed experimental report is provided for transparency.

---

## Report

📄 `ASD_Classification_Experimental_Report.pdf`

---

## Contributors

- **Milica Gojak**
- **Vladan Bašić** 
