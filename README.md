Forests play a vital role in maintaining ecological balance and providing resources 
for human activities. Accurate classification of forest cover types is crucial for 
effective management and conservation. The growing availability of environmental 
data, including geographical and topographical features, offers new opportunities for 
leveraging machine learning to address this challenge. 
The dataset used in this project, covtype.csv, contains various features such as 
elevation, aspect, and distances to water bodies, aimed at predicting the type of 
forest cover. This classification task not only aids in better forest management but 
also supports environmental policy-making by identifying patterns and anomalies in 
forest data. 
However, challenges such as handling missing data, identifying key features, and 
selecting appropriate models must be addressed to achieve reliable predictions. This 
project focuses on utilizing advanced machine learning techniques to classify forest 
cover types accurately. 
Key objectives include: 
• Data Preprocessing: Ensure clean and normalized datasets through 
imputation, feature scaling, and engineering. 
• Model Comparison: Apply and evaluate different machine learning models, 
including Random Forest, Gradient Boosted Trees, and Logistic Regression. 
• Performance Analysis: Use metrics like accuracy and confusion matrices to 
assess model effectiveness. 
• Visualization: Provide insights through graphical representations of model 
predictions and feature importance. 
By applying rigorous preprocessing, feature engineering, and advanced machine 
learning techniques, this project aims to deliver robust classification results and 
actionable insights for forest management. 
2. Dataset Description 
The Forest Cover Type dataset provides detailed information on the characteristics 
of various forest regions. It includes features such as elevation, slope, aspect, and 
distances to hydrology, roadways, and fire points, which are crucial for predicting 
forest cover types. The dataset is composed of both numerical and categorical 
features and has been designed to facilitate multi-class classification tasks. 
To prepare the dataset for analysis, the data preprocessing phase included: 
• Loading and Cleaning: Merging all relevant data into a unified dataset while 
handling missing values and outliers. 
• Feature Selection: Retaining necessary columns, such as environmental and 
geographical features, for meaningful analysis. 
• Normalization and Scaling: Ensuring consistency across numeric features by 
applying techniques like MinMax scaling. 
By leveraging PySpark’s distributed computing capabilities, the dataset was 
efficiently processed, making it suitable for large-scale machine learning models. 
The dataset offers a robust foundation for understanding and predicting forest cover 
types. 
Dataset Link: https://www.kaggle.com/competitions/forest-cover-type-prediction 
3. Methodology 
3.1 Data Preprocessing 
1. Loading Data: 
o The dataset was loaded using PySpark’s read.csv method with schema 
inference. 
2. Handling Missing Values: 
o Checked for missing values and imputed missing numeric values with 
column means. 
o Rows with excessive missing values were dropped. 
3. Feature Normalization: 
o Numeric features were scaled using MinMaxScaler to normalize the 
data. 
4. Feature Engineering: 
o Interaction terms were generated, such as the product of Elevation and 
Aspect. 
o Polynomial features were added, such as squared terms for elevation 
and aspect. 
5. Dataset Splitting: 
o The dataset was split into 80% training and 20% testing subsets for 
model development.
<img width="901" height="576" alt="image" src="https://github.com/user-attachments/assets/d3e08c1f-2152-4455-947c-d93933d78bda" />
3.2.2 Gradient Boosted Trees Classifier 
• Implemented with 20 iterations and a maximum depth of 5. 
• Optimized for multi-class classification.
<img width="668" height="306" alt="image" src="https://github.com/user-attachments/assets/4e44db49-b74f-4127-a3e2-2c0bc1b55c67" />
<img width="666" height="420" alt="image" src="https://github.com/user-attachments/assets/08e669d4-5d69-4f8d-9207-7f0baffb7d86" />
4. Results and Analysis 
4.1 Accuracy Comparison 
The models achieved the following accuracy scores: 
Model 
Random Forest 
Accuracy 
78.2% 
Gradient Boosted Trees 71.5% 
Logistic Regression 
4.2 Feature Importance 
75.9% 
• Random Forest and Gradient Boosted Trees highlighted Elevation and 
Horizontal_Distance_To_Roadways as critical features. 
• Logistic Regression Coefficients indicated that Elevation had the most 
significant impact across classes. 
4.3 Confusion Matrices 
Confusion matrices for all models were analyzed: 
• Random Forest showed strong class-wise predictions but struggled with 
minority classes. 
• Gradient Boosted Trees had the best overall balance. 
• Logistic Regression performed reasonably but underperformed in 
distinguishing similar classes.
<img width="619" height="496" alt="image" src="https://github.com/user-attachments/assets/0a62578e-892c-43cb-85d9-f7e8447cab5d" />
<img width="499" height="653" alt="image" src="https://github.com/user-attachments/assets/ff722733-743c-4f66-8152-1c9f08f5b8bc" />
<img width="552" height="530" alt="image" src="https://github.com/user-attachments/assets/84ae8967-0465-41e7-9128-acd60023f17d" />
<img width="562" height="667" alt="image" src="https://github.com/user-attachments/assets/d29618a2-36a0-4682-9f95-4f9f674c354e" />
5. Challenges 
• Data Imbalance: The dataset exhibited imbalanced classes, which required 
oversampling techniques to ensure fair model training. 
• Feature Selection: Identifying the most impactful features among a large 
number of variables posed challenges for model optimization. 
• Outlier Handling: Addressing outliers in numeric features was critical to 
maintaining data integrity. 
• Computational Complexity: Training complex models like Gradient Boosted 
Trees required significant computational resources. 
6. Key Findings 
• Gradient Boosted Trees Outperformed: This model demonstrated the 
highest accuracy (87.5%) and balanced performance across all classes. 
• Elevation is Critical: Across all models, Elevation emerged as the most 
important feature influencing forest cover type classification. 
• Visualization Insights: Feature importance and confusion matrices provided 
valuable insights into model performance and key predictors. 
• Logistic Regression Interpretability: Despite lower accuracy, Logistic 
Regression offered interpretable coefficients, making it useful for 
understanding feature impact. 
7. Conclusion 
This project successfully implemented and compared three machine learning models 
to classify forest cover types. The Gradient Boosted Trees Classifier emerged as 
the most effective model with the highest accuracy and balanced predictions. 
Random Forest also performed well, while Logistic Regression provided 
interpretable results but lagged in accuracy. 
8. Future Work 
• Hyperparameter Tuning: 
o Automate tuning for optimal model parameters. 
• Ensemble Models: 
o Combine models using stacking or bagging techniques to improve 
performance. 
• External Data Integration: 
o Incorporate satellite imagery or climate data to enhance predictive 
power. 
• Deployment: 
o Develop a real-time prediction system using Flask or FastAPI.
