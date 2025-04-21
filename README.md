# Ethically Sound Deep Learning Model for Credit Card Offer Acceptance Prediction

[![View in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1gG8JzH8A-pzs_9-vFtl4d9rJqHAZak-M?usp=sharing)

## 📌 Overview

This project develops and evaluates a **deep learning model** to predict whether a customer will accept a **credit card offer**, while placing a strong emphasis on **ethical AI practices**.

We address potential biases in the dataset, especially those related to **income-based discrimination**, and demonstrate how to create **fair, explainable, and trustworthy AI systems** using modern tools like SHAP, Fairlearn, and AIF360.

---

## 📊 Dataset

- Source: [Kaggle Credit Card Offer Dataset](https://www.kaggle.com/datasets/thedevastator/unlocking-credit-card-offer-acceptance-trends-in)
- Features: Income Level, Credit Rating, Average Balance, Mailer Type, Overdraft Protection, etc.
- Sensitive Attribute: `Income Level`

---

## ✅ Tasks Completed

1. **Initial Deep Learning Model**
   - 3-layer neural network
   - Trained using SMOTE-balanced data
   - Evaluated with F1 Score due to class imbalance

2. **Explainability using SHAP**
   - Visualizes feature impact for transparency
   - Shows model's decision-making logic

3. **Bias Detection with Fairlearn**
   - Detected unfair treatment across income groups

4. **Ethical Redesign**
   - **Reweighing (Fairlearn)**
   - **Adversarial Debiasing (AIF360)**
   - Compared fairness vs. performance

---

## 🧪 Results Summary

### 📊 **Performance Metrics by Income Group**

| Model            | Income Group       | Accuracy | Precision | Recall | F1 Score | Selection Rate |
|------------------|--------------------|----------|-----------|--------|----------|----------------|
| **Baseline**     | Low/Med Income     | 0.9005   | 0.0783    | 0.0523 | 0.0627   | 0.0425         |
|                  | High Income        | 0.9264   | 0.0541    | 0.0606 | 0.0571   | 0.0412         |
| **Reweighed**    | Low/Med Income     | 0.8690   | 0.0748    | 0.0930 | 0.0829   | 0.0792         |
|                  | High Income        | 0.8930   | 0.0435    | 0.0909 | 0.0588   | 0.0769         |
| **Adversarial**  | Low/Med Income     | 0.7281   | 0.0676    | 0.2558 | 0.1069   | 0.2408         |
|                  | High Income        | 0.8874   | 0.0405    | 0.0909 | 0.0561   | 0.0825         |

---

### 🧠 Insights

- **Baseline** model favors accuracy but is unfair — large disparity in treatment and selection rates.
- **Reweighed** model slightly drops accuracy but brings **excellent fairness** without big performance hits.
- **Adversarial Debiasing** makes the **strongest fairness push** (especially in selection rate balance and recall for the disadvantaged group) — but sacrifices accuracy, especially for low/medium-income groups.

---

| **Metric** | **Original Model** | **Baseline** | **Fair (Reweighed)** | **Adversarial Debiasing** |
|------------|--------------------|--------------|-----------------------|----------------------------|
| **Accuracy** | 0.8322 | 0.8544 | 0.9350 | 0.8208 |
| **Precision** | 0.1373 | 0.0701 | 0.1081 | 0.0473 |
| **Recall** | 0.3474 | 0.1268 | 0.0195 | 0.1122 |
| **F1 Score** | 0.1968 | 0.0903 | 0.0331 | 0.0666 |
| **ROC AUC** | — | 0.5167 | 0.5015 | 0.5141 |
| **Statistical Parity Diff** | 0.0087 | 0.0023 | -0.0129 | 0.1369 |
| **Disparate Impact** | 1.0769 | 0.9779 | 0.7904 | 123.7814 |
| **Equal Opp. Diff** | -0.0107 | 0.0655 | -0.0573 | 0.1221 |
| **Avg Odds Diff** | -0.0005 | — | -0.0344 | 0.1300 |
| **Theil Index** | 0.0871 | — | 0.0715 | 0.0840 |

---

## ⚖️ Key Ethical Takeaways

- Accuracy alone is **not sufficient**.
- **Fairness-aware techniques** like reweighing and adversarial debiasing can help mitigate bias.
- SHAP improves **transparency** and trust.
- Ethical trade-offs are necessary and application-dependent.

---

## 🛠️ Tools & Libraries

- Python, Pandas, Scikit-learn
- Keras + TensorFlow (Deep Learning)
- SHAP (Explainability)
- Fairlearn, AIF360 (Fairness)
- SMOTE (Balancing)

---

## ▶️ How to Run

1. Click the badge at the top or open the [Google Colab Notebook](https://colab.research.google.com/drive/1gG8JzH8A-pzs_9-vFtl4d9rJqHAZak-M?usp=sharing)
2. Follow the cells step-by-step to preprocess data, train the models, and evaluate performance and fairness.

---

## 📄 Report

[Report Link](https://drive.google.com/file/d/1yOM_W4oLlzpsxYt4bpPfrs4kzGDtS9g3/view?usp=sharing)

---

## 🧑‍🎓 Author

**Harshini V**  

