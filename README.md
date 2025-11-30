# Network Anomaly Detection

## Model Description

This project focuses on the design and implementation of an intelligent **network anomaly detection system** using machine learning techniques to identify malicious network activities. The **NSL-KDD dataset** was used for training and evaluation. Data preprocessing included handling missing values, encoding categorical features such as **protocol type, service, and flag** using one-hot encoding, and scaling numerical features using **standardization**.  

A **Random Forest classification model** was trained to perform **binary classification** between normal and malicious traffic. The model was evaluated using **accuracy, precision, recall, F1-score, and confusion matrices**, achieving high detection performance. The final trained model was exported in a deployable format and successfully integrated with an **API-based submission system for automated testing**.  

This project demonstrates practical skills in **network security, data preprocessing, feature engineering, model training, performance evaluation, and secure model deployment**.

---

## Why Use This Model?

Traditional network security systems often fail to detect **modern and unknown attacks** efficiently. This project aims to build an **intelligent anomaly detection system** using machine learning that can automatically classify network traffic as **normal or malicious** with high accuracy.

---

## Dataset Used

- **Dataset Name:** NSL-KDD  
- **Source:** NSL-KDD Dataset  
- **Type:** Network traffic records  
- **Features:** 41 network traffic attributes (categorical and numerical)  
- **Target:** Binary classification  
  - `0` → Normal  
  - `1` → Attack  

---

## Technologies & Tools Used

- **Programming Language:** Python  
- **Libraries:**
  - NumPy
  - Pandas
  - Scikit-learn
  - Matplotlib
  - Seaborn
  - Joblib  
- **Model Used:** Random Forest Classifier  
- **Platform:** Jupyter Notebook / Google Colab  

---

## Methodology

1. Downloaded and extracted the NSL-KDD dataset.  
2. Assigned proper column names to the raw data.  
3. Handled missing values.  
4. Encoded categorical features:
   - `protocol_type`
   - `service`
   - `flag`  
5. Scaled numerical features using `StandardScaler`.  
6. Created a binary target variable (`attack_flag`).  
7. Trained a **Random Forest Classifier**.  
8. Evaluated the model using:
   - Accuracy
   - Precision
   - Recall
   - F1-score
   - Confusion Matrix  
9. Exported the trained model using **Joblib** for deployment.  

---

## Results

- Achieved **high accuracy** on the test dataset.  
- Demonstrated strong performance in detecting malicious network traffic.  
- Confusion matrix and classification reports confirm effective classification.  

---

## Disclaimer

This project is adapted from the Hack The Box Academy module  
**“Applications of AI in InfoSec – Network Anomaly Detection”** and is used  
strictly for personal learning and educational practice.
