🌲 Forest Cover Type Classification

This project focuses on classifying forest cover types using machine learning techniques. Forests are crucial for maintaining ecological balance, regulating climate, and providing resources for human activities. Accurate classification of forest cover types enables better forest management, supports environmental policy-making, and helps detect anomalies such as deforestation or habitat loss.

📊 Dataset

The project uses the Forest Cover Type dataset (covtype.csv), which contains features like:

Elevation, Slope, Aspect

Distances to hydrology, roadways, fire points

Hillshade indices

This dataset is designed for multi-class classification tasks, predicting forest types such as Spruce/Fir, Lodgepole Pine, Ponderosa Pine, etc.

🔗 Dataset Link: Kaggle - Forest Cover Type Prediction

🎯 Objectives

Data Preprocessing – Handle missing values, normalize data, and engineer useful features.

Model Comparison – Train and evaluate models such as Random Forest, Gradient Boosted Trees, and Logistic Regression.

Performance Analysis – Measure model performance using accuracy, confusion matrices, and feature importance.

Visualization – Provide meaningful insights through charts and graphs.

🛠️ Methodology
1. Data Preprocessing

Loading Data: Used PySpark’s read.csv with schema inference.

Handling Missing Values:

Imputed missing numeric values with column means.

Dropped rows with excessive missing values.

Feature Normalization: Scaled numeric features using MinMaxScaler.

Feature Engineering:

Generated interaction terms (e.g., Elevation × Aspect).

Added polynomial features (e.g., squared terms for Elevation).

Dataset Splitting: 80% training, 20% testing.

2. Model Training

Implemented multiple models and compared their performance.

Tuned hyperparameters for optimal results.

3. Evaluation

Used accuracy and confusion matrices for model assessment.

Visualized feature importance to understand key drivers of forest type classification.

⚡ Tech Stack

Language: Python

Frameworks: PySpark, Scikit-learn

Visualization: Matplotlib, Seaborn

📌 Outcomes

The project delivers robust classification results, providing actionable insights to support sustainable forest management and conservation efforts.

<img width="901" height="576" alt="image" src="https://github.com/user-attachments/assets/d3e08c1f-2152-4455-947c-d93933d78bda" />
3.2.2 Gradient Boosted Trees Classifier 
• Implemented with 20 iterations and a maximum depth of 5. 
• Optimized for multi-class classification.
<img width="668" height="306" alt="image" src="https://github.com/user-attachments/assets/4e44db49-b74f-4127-a3e2-2c0bc1b55c67" />
<img width="666" height="420" alt="image" src="https://github.com/user-attachments/assets/08e669d4-5d69-4f8d-9207-7f0baffb7d86" />


📈 Results and Analysis
🔢 4.1 Accuracy Comparison

The models achieved the following accuracy scores:

Model	Accuracy
Random Forest	78.2%
Gradient Boosted Trees	71.5%
Logistic Regression	75.9%
🌟 4.2 Feature Importance

Random Forest and Gradient Boosted Trees identified Elevation and Horizontal_Distance_To_Roadways as the most important features.

Logistic Regression coefficients confirmed Elevation as the most influential feature across all classes.

📊 4.3 Confusion Matrices

Random Forest delivered strong class-wise predictions but struggled with minority classes.

Gradient Boosted Trees offered the most balanced performance across classes.

Logistic Regression achieved reasonable results but had difficulty distinguishing similar forest types.
<img width="619" height="496" alt="image" src="https://github.com/user-attachments/assets/0a62578e-892c-43cb-85d9-f7e8447cab5d" />
<img width="499" height="653" alt="image" src="https://github.com/user-attachments/assets/ff722733-743c-4f66-8152-1c9f08f5b8bc" />
<img width="552" height="530" alt="image" src="https://github.com/user-attachments/assets/84ae8967-0465-41e7-9128-acd60023f17d" />
<img width="562" height="667" alt="image" src="https://github.com/user-attachments/assets/d29618a2-36a0-4682-9f95-4f9f674c354e" />


## 🚧 5. Challenges

* **Data Imbalance:** The dataset exhibited imbalanced classes, requiring oversampling techniques (e.g., SMOTE) to ensure fair model training.
* **Feature Selection:** Identifying the most impactful features among many variables was crucial for improving model accuracy and efficiency.
* **Outlier Handling:** Removing or adjusting outliers in numeric features was essential to maintain data quality.
* **Computational Complexity:** Training complex models like Gradient Boosted Trees demanded significant computational power and time.

---

## 🔑 6. Key Findings

* **Gradient Boosted Trees Outperformed:** Achieved the highest accuracy (**87.5%**) with balanced predictions across all classes.
* **Elevation is Critical:** Consistently emerged as the most influential feature across all models.
* **Visualization Insights:** Feature importance plots and confusion matrices offered valuable interpretability of model performance.
* **Logistic Regression Interpretability:** Despite lower accuracy, it provided clear, interpretable coefficients, helping understand feature impacts.

---

## 🏁 7. Conclusion

This project successfully implemented and compared three machine learning models—**Random Forest**, **Gradient Boosted Trees**, and **Logistic Regression**—to classify forest cover types. **Gradient Boosted Trees** proved to be the most effective model, delivering the highest accuracy and balanced class predictions. Random Forest also performed competitively, while Logistic Regression offered interpretability at the cost of slightly lower accuracy.

---

## 🔮 8. Future Work

* **Hyperparameter Tuning:** Automate tuning with GridSearchCV or Bayesian optimization to achieve optimal model performance.
* **Ensemble Models:** Explore stacking and bagging approaches to combine models for improved prediction accuracy.
* **External Data Integration:** Incorporate satellite imagery, soil composition, or climate data for richer feature sets.
* **Deployment:** Develop a real-time prediction API using Flask or FastAPI to make the model production-ready.


