# Autism-Predictive-model-in-Children
## Overview
The aim of this project is to develop a machine learning model that accurately predicts the likelihood of a child having Autism Spectrum Disorder (ASD) based on various features. By identifying children at risk earlier, this model aims to support healthcare providers, parents, and caregivers in seeking timely interventions and treatments, thereby improving long-term outcomes.
## Business Understanding
### Business Problem
Autism Spectrum Disorder is often underdiagnosed, especially in younger children or those from diverse backgrounds. Early diagnosis can significantly improve intervention outcomes. Springwell Diagnostics wants a predictive model that identifies the likelihood of ASD early on, so it can be incorporated into their products and services, increasing market penetration and generating revenue.

### Stakeholder Audience
This project is designed for a hypothetical healthcare company, Springwell Diagnostics, which aims to enhance early detection of autism. The company is interested in investing in autism prediction research to develop a screening tool that can be integrated into routine health check-ups, providing substantial revenue potential while contributing to public health.

**Stakeholders**
1) Springwell Diagnostic Investors
2) Health providers and clinics
3) Parents and guardians
4) Public Health Organizations and Insurers

### Objectives

__*1) Evaluate ROI for Springwell Diagnostics:*__ Assess the potential return on investment by analyzing market demand, tool effectiveness, and revenue generation through subscriptions, partnerships, or sales.

__*2) Enhance Screening for Healthcare Providers and Clinics:*__  Provide a tool that clinics and hospitals can license or subscribe to, improving their screening processes and adding value to their services.

__*3) Offer Accessible Screening for Parents and Educators:*__  Make the tool available to parents and educators as a low-cost or freemium application, with basic features free and advanced options available for purchase.

__*4) Support Public Health Organizations and Insurers:*__  Enable bulk licensing for community-wide screening programs, creating a consistent revenue stream and supporting public health initiatives.

## Data Understanding

The [Child Autism Data](https://www.kaggle.com/datasets/ashishpawar511/autistic-spectrum-disorder-screening-for-children) is  a dataset obtained from kaggle and it contains the following information:
The dataset used for this project consists of 292 records of screening results from an autism screening app for children between the ages 4 to 11 years. The dataset includes features such as gender, age, ethnicity, family ASD history, and various questionnaire scores that help determine ASD likelihood.

***Key Features:***

* **Demographic Data:** Age, gender, ethnicity, etc.
* **Medical History:** Family ASD history, presence of jaundice, etc.
* **Screening Results:** Scores from ten behavioral screening questions.



### Correlation Heat Map
<h1 align="center">
  <img src="https://github.com/ElsieSerem/Autism-Predictive-model-in-Children/blob/main/Images/Correlation%20heat%20map.png?raw=true" alt="ABC Industries" height = 400 width="800" />
</h1>

Features with high correlation to the target variable are likely to significantly enhance the model’s performance. For this project, the A_scores show strong correlation and thus play a key role in establishing a robust baseline model. This helps in setting a solid foundation for evaluating and refining the model as additional complexity is introduced.

## Data Preparation
* **Data Cleaning:** Handled missing values and corrected data types.
* **Feature Engineering:** One-hot encoded categorical variables such as gender and ethnicity.
* **Target Variable:** Converted the Class/ASD column to binary values (1 for "Yes", 0 for "No").
* **Exploratory Data Analysis:** Identified key trends and patterns that informed feature selection and model choice.
## Modeling

Machine learning techniques were utilized to develop a predictive model for early detection of autism, leveraging its ability to identify complex patterns in data and improve diagnostic accuracy. This approach is ideal due to its capacity for effective pattern recognition, scalability, and efficiency, making it suitable for broad use in healthcare settings, schools, and public health programs.

### Model Selection and Comparison
To determine the best model for predicting autism, we evaluated three different machine learning algorithms: *Logistic Regression, Decision Tree, and Random Forest.* Each model was chosen for its unique strengths.

* **Logistic Regression** provides a straightforward approach to classification, particularly useful for understanding the impact of individual features.
* **Decision Tree** handles non-linear relationships and feature interactions effectively, making it suitable for more complex datasets.
* **Random Forest** builds on the strengths of Decision Trees by aggregating multiple trees, reducing overfitting, and improving overall predictive performance.

### Baseline Model Choice
Our analysis began by establishing a baseline model using Logistic Regression with the **A10_Score** feature, which showed a high correlation with the target variable **Class/ASD**. This feature was selected to create a simple yet effective benchmark for evaluating subsequent models.

### Model Performance and Evaluation
1) **Logistic Regression**

   * **Accuracy:** 93.2%
   * **Confusion Matrix**: Identified most cases correctly, with 36 true negatives, 3 false positives, 1 false negative, and 19 true positives.
   * **Classification Report:** High precision, recall, and F1-score, particularly for the positive class, suggesting strong performance in identifying cases of autism.
2) **Decision Tree**

   * **Accuracy:** 86.4%
   * **Confusion Matrix:** Demonstrated more misclassifications, particularly for the negative class, with 33 true negatives, 6 false positives, 2 false negatives, and 18 true positives.
   * **Classification Report:** Lower precision and recall for both classes compared to Logistic Regression, indicating less reliable performance.
3) **Random Forest**

   * **Accuracy:** 91.5%
   * **Confusion Matrix:** Showed strong performance similar to Logistic Regression, with 36 true negatives, 3 false positives, 2 false negatives, and 18 true positives.
   * **Classification Report:** Comparable precision, recall, and F1-score to Logistic Regression, confirming its effectiveness in balancing bias and variance.

### Selection
The Logistic Regression model emerged as the most accurate with an accuracy of 93.2%, outperforming both the Decision Tree and the Random Forest models. 

## Evaluation
### Model Evaluation Summary
Logistic Regression emerged as the best model due to its highest accuracy (93.2%), balanced performance, and simplicity. It outperformed the Random Forest (91.5% accuracy) and Decision Tree (86.4% accuracy), which showed more misclassifications.

### Evaluation Insights:

Logistic Regression has a high mean accuracy, indicating its effectiveness in generalizing to new, unseen data. The consistency in scores ranging from 0.896 to 0.949 suggests robust performance across different data subsets.

***Training and Validation Scores:*** The training score remains high and stable, showing that the model fits the training data well. The validation score initially lags but improves and stabilizes as more data is introduced, indicating reduced overfitting and enhanced generalization.

### Learning Curve
A learning curve is used to evaluate how a machine learning model's performance improves with additional training data and to diagnose issues like overfitting or underfitting. By comparing training and validation scores over time, it helps to understand whether a model is learning effectively, whether it needs more data or adjustments, and if its complexity is appropriate. Essentially, learning curves provide valuable insights into the model's ability to generalize and guide improvements for better performance.

### Graph showing Learning curve

<h1 align="center">
  <img src="https://github.com/ElsieSerem/Autism-Predictive-model-in-Children/blob/main/Images/Learning%20Curve.png?raw=true" alt="ABC Industries" height = 400 width="800" />
</h1>

***Interpratation:*** The initial low validation score compared to the high training score suggested potential overfitting. However, as the dataset grew, the validation score improved, reflecting better generalization and reduced overfitting.

## Conclusion
In conclusion, Logistic Regression is the preferred model due to its highest accuracy, balanced performance across classes, and strong generalization capabilities. It achieved the highest accuracy at 93.2% and demonstrated effective identification of autism cases with well-balanced precision and recall. Its ability to generalize well from the training data makes it the most reliable choice for practical applications, ensuring accurate and reliable predictions in real-world scenarios.








