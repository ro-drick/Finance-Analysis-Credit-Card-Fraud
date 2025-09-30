
# 💳 Credit Card Fraud Detection

The objective of this project is to forecast **fraudulent credit card transactions** using various machine learning models.

This project uses customer-level transaction data gathered and analyzed through a research partnership between **Worldline** and the **Machine Learning Group**.  
The dataset, sourced from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud), contains **284,807 transactions**, of which only **492 are fraudulent**. Due to the severe class imbalance, special handling is required before model development.

---

## 📌 Problem Statement

For many banks, retaining profitable customers is a primary business objective. However, banking fraud presents a significant threat across financial institutions.  
Fraudulent activities cause:

- Substantial **financial losses**  
- Reduced **trust and credibility**  
- Increased **operational risks**

According to the **Nilson Report**, global banking fraud was projected to cause **$30 billion in losses by 2020**. With the rise of digital payment channels, fraud is evolving in **new and complex ways**.

👉 Machine Learning offers proactive fraud prevention by:  
- Minimizing manual reviews  
- Reducing chargebacks and fees  
- Preventing false transaction denials  
- Enhancing customer trust  

---

## 📊 Dataset Overview

- **Source**: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- **Transactions**: 284,807 (European cardholders, September 2013, 2 days)  
- **Fraudulent cases**: 492 (~**0.172%** of total)  
- **Data Anonymization**: Features transformed using **PCA** for confidentiality  

### Features:
- `Time`: Seconds elapsed since the first transaction  
- `Amount`: Transaction amount  
- `V1, V2, …, V28`: PCA-derived components  
- `Class`: Target variable (0 = Non-fraud, 1 = Fraud)  

---

## 🔄 Project Pipeline

1. **Data Understanding**  
   - Load and explore dataset  
   - Identify key features for modeling  

2. **Exploratory Data Analysis (EDA)**  
   - Perform univariate & bivariate analysis  
   - Handle skewness if present  
   - Assess data distribution  

3. **Data Preparation**  
   - Train/Test split  
   - Apply **k-fold cross-validation** ensuring minority class representation  

4. **Model Building & Hyperparameter Tuning**  
   - Experiment with multiple ML models  
   - Test sampling techniques (e.g., **SMOTE, undersampling**)  
   - Optimize hyperparameters  

5. **Model Evaluation**  
   - Use metrics suitable for imbalanced data:  
     - Precision  
     - Recall  
     - F1-score  
     - ROC-AUC  
   - Focus on **minimizing false negatives** (missing fraud cases)  

---

## 🛠️ Technologies Used

- **Python 3.9+**  
- **Jupyter Notebook**  
- **Libraries**:  
  - `pandas`, `numpy` – Data manipulation  
  - `matplotlib`, `seaborn` – Visualization  
  - `scikit-learn` – Machine learning & evaluation  
  - `imblearn` – Sampling techniques (e.g., SMOTE)  

---

## ⚡ How to Run

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your-username/credit-card-fraud-detection.git
   cd credit-card-fraud-detection
```

2. **Create a virtual environment & activate it**

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Mac/Linux
   venv\Scripts\activate      # On Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Download the dataset**

   * Get the dataset from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud)
   * Place it in the `data/` folder

5. **Run the Jupyter Notebook**

   ```bash
   jupyter notebook
   ```

## 🚀 Key Goals

* Build a **robust fraud detection model**
* Effectively handle **class imbalance**
* Optimize for **real-world banking applications**

---

## 📌 Future Work

* Implement **deep learning models** (LSTM/Autoencoders)
* Explore **real-time fraud detection pipelines**
* Deploy the model using **Flask/FastAPI**

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repo, open issues, or submit pull requests.

---

## 📜 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

