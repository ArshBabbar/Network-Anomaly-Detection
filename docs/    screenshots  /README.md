# Project Screenshots

This section provides visual evidence of the successful execution and evaluation of the Network Anomaly Detection pipeline.

---

## Dataset Preview (NSL-KDD)

![Dataset Preview](dataset_overview.png)

This screenshot shows the first few rows of the NSL-KDD dataset after loading it into a pandas DataFrame.  
It confirms correct column mapping, presence of categorical and numerical features, and availability of attack labels used for classification.

---

## Model Evaluation Results

![Model Evaluation](model_evaluation.png)

This screenshot demonstrates the final evaluation of the trained Random Forest model on the test dataset.  
It includes overall accuracy, precision, recall, F1-score, and a confusion matrix for multi-class network attack detection (Normal, DoS, Probe, Privilege, Access).

The results verify that the model was successfully trained and evaluated using real network traffic data.
