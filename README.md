# 🧬 Data Mining Pipeline for B-Cell Epitope Prediction in *Trypanosoma cruzi*

### Using CRISP-DM: Machine Learning, EDA, Preprocessing, Feature Selection, Hyperparameter Tuning & Evaluation

This project presents a computational pipeline developed in **Python** for predicting B-cell epitopes in *Trypanosoma cruzi*, the parasite responsible for Chagas disease. The work follows the **CRISP-DM** methodology and incorporates a range of data mining techniques from exploratory data analysis to final model deployment.

---

## 📈 Overview of the CRISP-DM Pipeline

**CRISP-DM (Cross-Industry Standard Process for Data Mining)** was used as the guiding methodology:

* ✅ **Business Understanding** – Define the goal: predict potential B-cell epitopes in *T. cruzi* proteins.
* 📊 **Data Understanding** – Perform exploratory data analysis (EDA) on a high-dimensional biological dataset.
* 🧹 **Data Preparation** – Clean, scale, balance, and reduce dimensionality using both filter and embedded feature selection methods.
* 🤖 **Modeling** – Train and evaluate machine learning models.
* 🧪 **Evaluation** – Compare model performance using multiple metrics.
* 🚀 **Deployment** – Final pipeline applied to protein data for epitope prediction.

---

## 🔍 Exploratory Data Analysis & Preprocessing

* Conducted **comprehensive EDA** to uncover patterns, data distribution, and class imbalance.
* Cleaned data, handled missing values, scaled features, and applied multiple class balancing techniques:

  * **Undersampling**, **Oversampling**, and **SMOTE**.

### 📊 Visual Insights from EDA

| Analysis                          | Graph                                                                                |
| --------------------------------- | ------------------------------------------------------------------------------------ |
| Missing values per column         | ![](https://github.com/usman-Iqbal-5/data-mining-pipeline/Images/missing-values-per-column) |
| Missing values per row            | ![](https://github.com/user-attachments/assets/cc60e69d-6173-438c-adf1-c94abae4b60f) |
| Feature value spread (max vs min) | ![](https://github.com/user-attachments/assets/401ffc7f-b58d-4711-bf29-d355586fde64) |
| Class imbalance                   | ![](https://github.com/user-attachments/assets/7a220a80-e5f7-40ee-93df-48246ea6e94f) |

---

### 🧠 Feature Selection

To improve model performance and reduce overfitting in this high-dimensional dataset, feature selection was performed using both **filter** and **embedded** methods:

#### ✅ Filter Method – Information Gain

* **Information Gain** was computed for each feature relative to the target variable (epitope/non-epitope).
* The top 10 most informative features were selected for initial model training.

  <img width="606" alt="Information Gain - Top Features" src="https://github.com/user-attachments/assets/e4eff02a-3ca9-4f72-bd67-ac8f2e5da589">

#### ✅ Embedded Method – Random Forest Feature Importance

* A **Random Forest classifier** was trained and its built-in feature importance scores were used to evaluate the contribution of each feature.
* The top 15 features were identified, based on how much they helped differentiate between the classes.

  <img width="608" alt="Random Forest Feature Importance" src="https://github.com/user-attachments/assets/87c7a448-427f-4c71-b70f-a7ee1bee2d79">

These selected features were used to:

* Reduce computational complexity
* Improve training time
* Enhance model interpretability
* Maintain or improve prediction performance

---

## 🤖 Model Development

* Built and tested several ML algorithms:

  * **Decision Tree**, **Random Forest**, **Support Vector Machine**, **Logistic Regression**, and **Artificial Neural Network**.
* Evaluated models using:

  * **Balanced Accuracy**
  * **Precision**
  * **Recall**
  * **F1-Score**

---

## 🧬 Epitope Prediction Pipeline

* Developed a **functional programming-style pipeline** for B-cell epitope prediction using the best-performing model.
* Applied the model to unseen protein data to generate potential epitope candidates.

![Epitope prediction pipeline](https://github.com/user-attachments/assets/f63c8d7d-b768-42cd-b08e-81c268399f85)

---

## 🚀 Getting Started

To clone and explore this project:

```bash
git clone https://github.com/Usman-A-Iqbal/Data-Mining-Pipeline-for-B-Cell-Epitope-Prediction-in-Trypanosoma-cruzi-Using-CRISP-DM
```

> ⚠️ This notebook was designed to run on **Google Colab**, which supports GPU acceleration.

---

## 🛠️ Tools and Technologies Used

* **Python**
* **Scikit-Learn**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Google Colab**
* **Jupyter Notebook**
* **CRISP-DM Methodology**
* **GPU Acceleration (for model training)**

---

## 📚 Key Takeaways

* Demonstrated ability to implement **real-world ML pipelines** in a **biomedical context**.
* Gained practical experience in:

  * High-dimensional data handling
  * Class balancing and feature selection
  * Model evaluation and optimization
  * Functional pipeline development in Python
* Reinforced the use of **CRISP-DM** as a robust methodology for data mining projects.

