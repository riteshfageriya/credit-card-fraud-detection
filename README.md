# ML-for-Credit-Card-Fraud-Detection

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
- **SVM (Support Vector Machine):** Chosen for its effectiveness in high-dimensional spaces, ideal for distinguishing fraudulent transactions in complex datasets.
- **XGBoost:** Known for its high performance in classification tasks, handling class imbalance, and focusing on difficult cases.
- **PCA (Principal Component Analysis):** Reduces the dataset's dimensionality, improving both speed and efficiency while maintaining important data variance.
- **SMOTE (Synthetic Minority Over-sampling Technique):** Balances the dataset by generating synthetic samples for underrepresented (fraudulent) classes, preventing model bias.
- **Ensemble VotingClassifier:** Combines SVM and XGBoost, leveraging their strengths for better overall performance by averaging predicted probabilities.
- **GridSearchCV & RandomizedSearchCV:** Used for hyperparameter tuning to optimize model performance.

### Challenges & Future Work:
- **Challenges:**
  - **Class imbalance:** Fraudulent transactions are a small minority, making accurate detection challenging. SMOTE was used to improve balance, but further refinement is needed.
  - **Computation time:** Training models, especially during hyperparameter tuning and ensemble building, can be time-consuming, affecting real-time applicability.
  - **Overfitting:** Preventing overfitting and ensuring models generalize well to unseen data is a continuous focus, with PCA helping mitigate this.

- **Future Work:**
  - **Real-time fraud detection:** Optimizing the system for real-time detection to handle continuous transaction streams.
  - **Feature engineering:** Exploring advanced techniques to extract more meaningful features and boost model performance.
  - **Explainability:** Incorporating tools like SHAP or LIME to improve model transparency and explainability in fraud detection.
  - **Advanced ensembling:** Implementing stacking methods, where the output of one model feeds into another, to further improve accuracy.


