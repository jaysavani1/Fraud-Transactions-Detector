# Transaction Fraud Detector
![image search api](https://altoo.io/live01/wp-content/uploads/2024/01/transaction-banking.jpg.webp)
---
## 1.0 Business Context

Blocker Fraud Company specializes in detecting fraudulent transactions on mobile platforms. Their flagship service, *Blocker Fraud*, guarantees the identification and blocking of fraudulent activity.

Operating under a performance-based service model, the company’s revenue is tied to the accuracy of its fraud detection. To rapidly grow its footprint in Brazil, Blocker Fraud has adopted a bold business strategy:

* **25%** commission on successfully detected fraudulent transactions.
* **5%** commission on transactions flagged as fraud but later verified as legitimate.
* **100% reimbursement** to customers for fraudulent transactions that are incorrectly classified as legitimate.

This strategy benefits clients by mitigating fraud losses while holding Blocker Fraud accountable for detection errors. However, it introduces financial risk for the company, making high model accuracy critical for profitability.

---

## 2.0 Business Assumptions

Fraud prevention strategies aim to minimize financial and reputational losses by identifying suspicious behavior in both digital and physical financial systems.

As fraud evolves, investment in cybersecurity has surged. According to the [2020 Banking Technology Survey by Febraban](https://blog.simply.com.br/tecnologia-bancaria-2020/), fraud-related losses in Brazil can total R\$1 billion annually — nearly half of what banks invest in security technology.

---

Here’s the **“Solution Approach”** section rewritten in a clear, professional table format for better readability and presentation:

---

## 3.0 Solution Approach

| **Step**                               | **Description**                                                                                                                                                                                   |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Data Exploration**                | Acquire and explore the dataset. Handle missing values and perform descriptive statistical analysis (mean, median, standard deviation, skewness, kurtosis, etc.) to understand data distribution. |
| **2. Feature Engineering**             | Generate new features based on hypotheses formed using a mind map. These features are aimed at improving model performance and supporting exploratory analysis.                                   |
| **3. Data Filtering**                  | Remove irrelevant or misleading data, such as non-human ages or hashed IDs, that do not contribute to fraud detection.                                                                            |
| **4. Exploratory Data Analysis (EDA)** | Conduct univariate, bivariate, and multivariate analysis to validate hypotheses and uncover patterns in the data.                                                                                 |
| **5. Data Preparation**                | Transform data to make it suitable for modeling. This may include encoding categorical features, rescaling numerical variables, and applying oversampling or undersampling techniques.            |
| **6. Feature Selection**               | Use algorithms like Boruta to identify and retain the most impactful features, reducing dimensionality and mitigating overfitting.                                                                |
| **7. Model Training**                  | Train multiple machine learning algorithms using cross-validation to assess performance and select the best candidate model.                                                                      |
| **8. Hyperparameter Tuning**           | Optimize the selected model’s parameters to improve accuracy and generalization. Evaluation metrics from the previous step are reused here.                                                       |
| **9. Business Validation**             | Evaluate the model on unseen data and answer key business questions to assess real-world applicability and value.                                                                                 |
| **10. Model Deployment**               | Package the final model and supporting functions into a Flask API, preparing it for deployment in a production environment.                                                                       |

---

## 4.0 Key Data Insights

* **Fraudulent transactions tend to exceed R\$10,000.**
  ✔️ *True*: Most fraud cases involve amounts over \$10,000. However, some legitimate transactions also exceed \$100,000.
* **60% of fraudulent transactions are cash-out operations.**
  ❌ *False*: Fraud primarily occurs through both *cash-out* and *transfer* types, with nearly equal distribution.
* **Transactions over \$100,000 are mainly transfers.**
  ❌ *False*: While transfers are common, high-value transactions also occur in *cash-in* and *cash-out* types.
---

## 5.0 Business Outcomes

* **Revenue from correctly detected fraud**:
  Estimated income of **\$60,613,782.88** by identifying real fraud cases.

* **Revenue from false positives (legitimate flagged as fraud)**:
  Additional income of **\$183,866.98** due to conservative detection.

* **Loss from undetected frauds (false negatives)**:
  Refund obligations of **\$3,546,075.42** for incorrect approvals of fraudulent transactions.

* **Expected precision and accuracy on unseen data**:
  Balanced accuracy: **91.5%**, Precision: **94.4%**

* **Model reliability**:
  The model correctly identifies **82.9%** of fraud cases on unseen data.

* **Projected revenue with full-scale model use**:
  **\$60,797,649.86** — significantly higher than the **\$0** under the current method.

* **Projected loss under model deployment**:
  **\$3,546,075.42** — compared to **\$246,001,206.94** with the current method.

* **Net profit forecast using the model**:
  **\$57,251,574.44** — compared to a **\$246M loss** using existing methods.

---

## 6.0 Conclusion

Despite the highly imbalanced nature of the dataset, a robust and reliable model was developed. The projected business impact — a potential profit exceeding \$57 million — highlights the tangible value data science can bring to financial services.

---

## 7.0 Key Takeaways

* Effective fraud detection is possible even with extreme class imbalance.
* Models can be trained to detect rare classes representing <1% of the data.
* Precision in modeling can directly translate into substantial business value.

---

## 8.0 Next Steps

* Expand hypothesis testing with up to 10 new ideas.
* Explore additional oversampling or undersampling techniques.
* Deploy the final API to a production platform such as Heroku.

---

