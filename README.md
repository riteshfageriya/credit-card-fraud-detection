# ML-for-Credit-Card-Fraud-Detection

**DATASET: https://media.geeksforgeeks.org/wp-content/uploads/20240904104950/creditcard.csv**

## Main Challenges in Credit Card Fraud Detection

- **Enormous data** processed daily requires fast models to respond to fraud in real-time
- **Imbalanced data**, with 99.8% of transactions being non-fraudulent, makes detecting fraud difficult
- **Limited data availability** as most data is private
- **Misclassified data** where not all fraudulent transactions are caught and reported
- **Adaptive techniques** used by fraudsters against detection model

## Tackling the Challenges

- Use **simple, fast models** to quickly detect and classify anomalies as fraudulent
- Deal with imbalance using appropriate methods like oversampling, undersampling, or cost-sensitive learning
- Reduce **data dimensionality** to protect user privacy while maintaining performance
- Use **trustworthy data sources** to train more accurate models[
- Make models **simple and interpretable** to adapt quickly when fraudsters change tactics

Here's a slightly more detailed version for your README:

---

## What the application does:

This project focuses on detecting credit card fraud using machine learning techniques. The application preprocesses transaction data by applying PCA for dimensionality reduction and uses SMOTE to handle class imbalance. The main models used are SVM and XGBoost, which are combined into an ensemble using soft voting to enhance prediction robustness. The model evaluates performance through key metrics such as Accuracy, Precision, Recall, F1-Score, Matthews Correlation Coefficient (MCC), and AUC-ROC.

### Technologies Used:
- **SVM (Support Vector Machine):** Efficient in high-dimensional spaces, ideal for detecting fraudulent transactions in complex datasets.
- **XGBoost:** Known for high performance in classification, handling class imbalance, and focusing on difficult cases.
- **PCA (Principal Component Analysis):** Reduces dimensionality to enhance computation speed and maintain data variance.
- **SMOTE (Synthetic Minority Over-sampling Technique):** Balances the dataset by generating synthetic samples for minority (fraudulent) classes, mitigating bias.
- **Ensemble VotingClassifier:** Combines SVM and XGBoost, using soft-voting to leverage their strengths for improved accuracy.
- **GridSearchCV & RandomizedSearchCV:** Applied for hyperparameter tuning to optimize model performance.
- **Threshold Tuning:** Optimized the precision-recall threshold to improve key metrics like precision and F1-Score.

### Challenges & Future Work:
- **Challenges:**
  - **Class imbalance:** Fraud transactions are rare. SMOTE improved balance, but further refinement is needed for better precision and recall.
  - **Computation time:** Training, especially during hyperparameter tuning, is time-consuming. Optimizing for real-time use remains a focus.
  - **Overfitting:** PCA helps reduce overfitting, but continuous effort is needed to ensure generalization on unseen data.
  

- **Future Work:**
  - **Real-time fraud detection:** Optimizing the system for real-time fraud detection in continuous transaction streams.
  - **Feature engineering:** Exploring advanced techniques to extract better features and boost model performance.
  - **Explainability:** Using tools like SHAP or LIME to improve model transparency and explain fraud detection decisions.
  - **Advanced ensembling:** Implementing stacking methods to further improve accuracy by combining multiple models.

