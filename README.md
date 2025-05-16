# Credit-Card-Fraud-detection
# 💳 Credit Card Fraud Detection Using Machine Learning

This project focuses on detecting fraudulent credit card transactions using Machine Learning techniques. It compares the performance of Random Forest, XGBoost, and Support Vector Machine (SVM) models on a highly imbalanced dataset of real transactions.

---

## 🧾 What is Credit Card Fraud?

Credit card fraud involves unauthorized use of a credit card to obtain goods or services. With the rise of digital payments, fraud has become increasingly complex, requiring automated systems capable of identifying suspicious patterns in real time.

---

## 📂 Dataset Description

- **Source**: Real-world anonymized credit card transactions  
- **Size**: ~550,000 records  
- **Features**:  
  - `Time` (elapsed seconds from the first transaction)  
  - `Amount` (transaction amount)  
  - 28 anonymized features (V1 to V28) from PCA  
  - `Class`:  
    - 0 → Legitimate  
    - 1 → Fraudulent  

> **Note**: The dataset is heavily imbalanced with less than 0.2% fraud cases.

---

## 🧹 Data Preprocessing

1. **Null Value Check**: Ensured dataset was clean and complete.  
2. **Outlier Handling**: Identified unusual values in features like `Amount`.  
3. **Feature Scaling**: Applied normalization/standardization.  
4. **Class Balancing**: Used **SMOTE (Synthetic Minority Oversampling Technique)** to balance the dataset.  
5. **Train-Test Split**: 80% training and 20% testing.

---

## 🤖 Machine Learning Models Used

### 1. 🌲 Random Forest Classifier
- Ensemble of decision trees
- Good at handling non-linear relationships
- Handles imbalanced data relatively well
- Accuracy achieved: **88.62%**

### 2. 🚀 XGBoost Classifier
- Gradient Boosting algorithm with regularization
- High performance, fast, and efficient
- Best model in this project
- Accuracy achieved: **90.00%**

### 3. 📉 Support Vector Machine (SVM)
- Classifier that uses hyperplanes to separate classes
- Works well on small to medium datasets
- Accuracy achieved: **86.50%**
- Less scalable for large datasets

---

## 🔁 Cross-Validation

- **Technique**: RepeatedKFold (5 folds, 2–10 repeats)  
- Ensures robust evaluation and reduces overfitting  
- Model performance was averaged over multiple folds

---

## 📊 Evaluation Metrics

| Metric         | Description                                               |
|----------------|-----------------------------------------------------------|
| **Accuracy**   | Percentage of correctly predicted transactions            |
| **Precision**  | % of flagged frauds that were actually fraud              |
| **Recall**     | % of actual frauds correctly detected                     |
| **F1 Score**   | Harmonic mean of precision and recall                     |
| **ROC AUC**    | Trade-off between true positives and false positives      |
| **Confusion Matrix** | Visual tool showing TP, FP, FN, TN                |

---

## 🧪 Results

| Model         | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|---------------|----------|-----------|--------|----------|----------|
| **XGBoost**   | 90.00%   | High      | High   | High     | High     |
| **Random Forest** | 88.62% | Good  | Good   | Good     | Good     |
| **SVM**       | 86.50%   | Moderate  | Moderate| Moderate| Moderate |

---

## ✅ Key Takeaways

- XGBoost delivered the **best performance** overall.
- All models benefited from **SMOTE** and **cross-validation**.
- Fraud detection can be **significantly improved** using tailored ML models.
- Real-world applicability in **banking**, **e-commerce**, and **payment gateways**.

---

## 🔮 Future Work

- Real-time fraud detection deployment via APIs  
- Integration of Deep Learning models (LSTM, Autoencoders)  
- Explainable AI for decision transparency  
- Continuous learning from live transaction streams

---


