## ⚙️ Machine Learning (ML)

- Machine Learning is a subset of AI that uses statistical algorithms to build models that can make predictions or decisions based on historical data. 

---

### 1. The Three Pillars of Learning

In 2025, we categorize ML based on the "signal" the model receives during training.

| Type | Analogy | Data Type | Common Use Case |
| :--- | :--- | :--- | :--- |
| **Supervised** | Learning with a Teacher | Labeled (Input + Answer) | Spam detection, Price prediction. |
| **Unsupervised** | Self-Discovery | Unlabeled (Raw data) | Customer segments, Anomaly detection. |
| **Reinforcement** | Trial and Error | Feedback (Rewards/Penalties) | Game AI, Robotics, Self-driving. |

---

### 2. Core ML Algorithms

- To solve different problems, we use different mathematical structures:

#### **A. Regression (Predicting Numbers)**
* **Linear Regression:** Predicting a continuous value (e.g., "What will this house cost?").
* **Polynomial Regression:** Used when the relationship between data points is curved rather than a straight line.

#### **B. Classification (Predicting Categories)**
* **Logistic Regression:** Despite the name, it's for classification (e.g., "Is this email spam? Yes/No").
* **Decision Trees:** A flowchart-like structure that makes decisions based on feature values.
* **Random Forest:** An "Ensemble" method that combines hundreds of decision trees to get a more accurate, stable result.
* **SVM (Support Vector Machines):** Finds the "boundary line" that best separates different classes in high-dimensional space.

#### **C. Clustering & Patterns**
* **K-Means Clustering:** Groups similar data points together into "K" number of clusters.
* **PCA (Principal Component Analysis):** Simplifies complex data by reducing the number of variables while keeping the most important information.

---

### 3. The ML Development Lifecycle (2025 Standard)

Building a model isn't just about code; it's a multi-step factory process:

1.  **Problem Definition:** Defining what you want to predict and how you will measure success.
2.  **Data Collection & Cleaning:** The most time-consuming step (approx. 80%). Removing "noise," handling missing values, and fixing errors.
3.  **Feature Engineering:** Selecting and transforming raw data into meaningful inputs (e.g., converting a "Date" into "Day of the Week").
4.  **Model Selection & Training:** Choosing the right algorithm and letting it "study" the data.
5.  **Evaluation:** Testing the model on data it has **never seen** before to check for accuracy.
6.  **Deployment & Monitoring:** Pushing the model to production and watching for **Data Drift** (when the real world changes and the model becomes less accurate).

---

### 4. Key Metrics: How do we know it works?

We don't just say a model is "good." We use specific math:

* **Accuracy:** Percentage of total correct guesses. (Caution: Misleading for imbalanced data!)
* **Precision:** "Of all the times I predicted 'Spam', how many were actually spam?"
* **Recall:** "Of all the actual spam emails, how many did I successfully catch?"
* **F1-Score:** The balance between Precision and Recall.
* **MSE (Mean Squared Error):** The average squared difference between predicted and actual values (used in Regression).

---

### 5. Overfitting vs. Underfitting

* **Underfitting:** The model is too simple and fails to learn the patterns (High Bias).
* **Overfitting:** The model "memorizes" the training data too perfectly and fails to generalize to new data (High Variance).

---
