# 🔐 Cybersecurity Threat Detection with Machine Learning

Combining system logs and network traffic data to detect and classify cybersecurity threats using machine learning. This capstone explores supervised models—including logistic regression, SVMs, and random forests—to improve performance, reduce false alarms, and support better security decisions at scale.

---

## 📁 Project Structure
---

## 🧠 Project Goals

- Investigate whether combining host-level logs and network traffic improves threat detection
- Apply machine learning to multiclass and multi-label classification tasks
- Improve model interpretability and reduce false positives
- Explore PCA, regularization, and tree-based modeling for high-dimensional and imbalanced data

---

## 🗃️ Datasets Used

| Dataset | Description |
|---------|-------------|
| **BETH** | Host logs with process metadata (benign, suspicious, malicious) |
| **UNSW-NB15** | Network flows labeled by attack type (e.g., DoS, Recon, Worm) |
| **Cybersecurity Attacks** | Action severity + metadata (engineered target) |
| **DrSufi CyberData** | Ranked multi-label threats (supports regression and multi-label classification) |

---

## ⚙️ Models Applied

### Regression
- Polynomial & interaction features
- Lasso, Ridge, Elastic Net
- Principal Component Regression (PCR)
- Stepwise feature selection (AIC)

### Classification
- Logistic Regression
- Support Vector Machines (SVM: linear & RBF)
- Decision Trees
- Random Forests

---

## 📊 Key Results

| Dataset | Model | Accuracy |
|---------|-------|----------|
| BETH | Random Forest | 99.2% |
| UNSW-NB15 | Random Forest | 91.1% |
| Cybersecurity Attacks | SVM / RF | 100% (possible label leakage) |
| DrSufi (Regression) | Elastic Net | MSE ≈ 0.000426 |

- PCA achieved strong variance compression (BETH: 95% in 6 components)
- Elastic Net selected a sparse, interpretable feature set
- SHAP and feature importances provided transparency for threat factors

---

## 📌 Notebooks

You can view and run all model development and EDA notebooks in the [`/notebooks`](./notebooks/) folder.

Example topics:
- `01_eda_beth.ipynb`
- `02_logistic_unsw.ipynb`
- `03_random_forest_attacks.ipynb`
- `04_regression_drsufi.ipynb`

---

## 📈 Future Work

- Add XGBoost for further performance benchmarking
- Apply SMOTE or reweighting to address class imbalance
- Evaluate model robustness with noisy/real-world data
- Explore streaming detection systems for real-time alerts

---

## 📚 References

- Highnam, K. (2023). *BETH Dataset* — [Kaggle](https://www.kaggle.com/datasets/katehighnam/beth-dataset)  
- Moustafa, N. & Slay, J. (2015). *UNSW-NB15* — [UNSW Canberra Cyber](https://www.unsw.adfa.edu.au/unsw-canberra-cyber/cybersecurity/ADFA-NB15-Datasets/)  
- Géron, A. (2019). *Hands-On ML with Scikit-Learn, Keras, and TensorFlow*  
- Hastie, Tibshirani & Friedman (2009). *The Elements of Statistical Learning*  

---

## 👋 About the Author

**Josh Laubach**  
M.S. Data Science, Boston University  
Professional Math Tutor | Data Scientist in Training  
📧 josh.laubach1@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/josh-laubach)
