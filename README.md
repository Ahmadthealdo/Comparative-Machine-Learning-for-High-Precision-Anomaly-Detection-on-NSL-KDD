# Comparative-Machine-Learning-for-High-Precision-Anomaly-Detection-on-NSL-KDD

This repository contains a high-precision, machine learning-based framework for detecting network intrusions using the **NSL-KDD dataset**. The project implements a unique **preprocessing-consistent pipeline** designed to maximize operational reliability and reduce "alert fatigue" in resource-constrained environments.

## 🚀 Key Features

* **Joint-Space Label Encoding**: A specialized strategy that fits encoders on the combined training and testing feature space to prevent "unseen label" errors.
* **High-Precision Results**: Achieves an exceptional **99.11% precision** with Random Forest, resulting in only **88 false positives** across the test set.
* **Comparative Analysis**: Provides a head-to-head performance evaluation between **Random Forest**, **XGBoost**, **KNN**, and **Logistic Regression**.
* **Explainable AI**: Includes feature importance ranking to identify primary drivers of classification, such as byte volumes (`src_bytes`) and service consistency.

## 📊 Performance Summary

| Algorithm | Accuracy | Precision | Recall | F1-Score |
| --- | --- | --- | --- | --- |
| **Random Forest** | 92.81% | **99.11%** | 86.42% | 0.9233 |
| **XGBoost** | **94.00%** | 99.08% | **88.86%** | 0.9369 |
| **KNN** | 92.63% | 99.07% | 86.10% | 0.9214 |
| **Logistic Regression** | 89.22% | 95.13% | 82.72% | 0.8850 |

## 🛠️ Installation & Usage

1. **Clone the repository**:
```bash
git clone https://github.com/AhmadAbdullah/Comparative-Machine-Learning-for-High-Precision-Anomaly-Detection-on-NSL-KDD.git
cd Comparative-Machine-Learning-for-High-Precision-Anomaly-Detection-on-NSL-KDD

```


2. **Install dependencies**:
```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn

```


3. **Prepare the Data**:
Ensure the `KDDTrain+.txt` and `KDDTest+.txt` files from the NSL-KDD dataset are in the project directory.
4. **Run the Analysis**:
```bash
python main.py

```



## 🧠 Methodology

This framework utilizes a robust pipeline to ensure stable feature encoding:

1. **Binary Transformation**: Converts multi-class labels into a simplified 0 (Normal) and 1 (Anomaly) format.
2. **Consistent Encoding**: Maps categorical features across the global feature space to ensure reliable generalization to unseen labels.
3. **Feature Scaling**: Employs `StandardScaler` to normalize background network "noise".

## 📜 License

This project is licensed under the **Apache License 2.0**. This aligns with the licensing of the NSL-KDD dataset used in the study.

## 👨‍💻 Author

**Ahmad Abdullah**

## 📝 Citation

If you use this framework in your research, please cite:


---
Dataset Citation:
S. A. Shariati, "NSL-KDD intrusion detection dataset," Kaggle, [Online]. Available: https://www.kaggle.com/datasets/shujaatalishariati/nsl-kdd-intrsuin-detection-dataset. (Accessed: Feb. 13, 2026).
