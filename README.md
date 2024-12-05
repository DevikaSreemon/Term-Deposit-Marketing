**Customer Term Deposit Subscription Prediction**

By Devika Sreemon

Apziva id: tlnKeryg0pda6D4N

**Overview**

The project aims to predict whether a customer will subscribe to a term deposit (variable y) based on various customer attributes. The dataset is sourced from a European banking institution's direct marketing campaign, and the goal is to build a machine learning model that can help optimize marketing strategies by identifying customers who are likely to subscribe to a term deposit.

The initial parts involves Exploratory Data Analysis and building a machine learning model, that aligns with the business goal of maximizing customer retention. Also reduce unnecessary calls by indentifying unsubscribing customers. 

Once we identify the customers most likely to purchase the investment product then we determine the key customer segments our client should prioritize. Additionally, we seek to uncover the driving factors behind purchase decisions, using clustering techniques (K-Means and Hierarchical Clustering) highlighting the features that should be emphasized for targeted marketing and engagement strategies.


**Table of Contents**

1. Project Description
2. Data Description
3. Exploratory data analysis
4. Modeling Process
5. Clustering
6. Results
7. Requirements
8. Conclusion

**1. Project Description**

The project involves the analysis of customer data obtained from a bank's marketing campaign and identify groups of customers who are more likely to subscribe to a term deposit. This will enable the bank to focus their marketing efforts on potential customers, improving efficiency and reducing costs.

**2. Data Description**

The dataset contains the following features:

age: Age of the customer (numeric)

job: Job type (categorical)

marital: Marital status (categorical)

education: Education level (categorical)

default: Whether the customer has credit in default (binary)

balance: Average yearly balance in euros (numeric)

housing: Whether the customer has a housing loan (binary)

loan: Whether the customer has a personal loan (binary)

contact: Type of communication used for contact (categorical)

day: Last contact day of the month (numeric)

month: Last contact month of the year (categorical)

duration: Duration of the last contact in seconds (numeric)

campaign: Number of contacts during the campaign (numeric)

y: Target variable indicating whether the customer subscribed to a term deposit (binary)


**3. Exploratory Data Analysis**

Step 1: Data Overview

Inspect the structure of the dataset to understand the number of rows and columns. Check for missing values in each column and assess their impact on the analysis.
Generate summary statistics for numeric variables (e.g., mean, median, standard deviation) and frequency counts for categorical variables.

Step 2: Univariate Analysis

Numerical Variables: Analyze distributions (e.g., histograms, box plots) of age, balance, duration, and campaign.

Categorical Variables: Plot bar charts for job, marital, education, contact, and month to examine category frequencies.

Step 3: Bivariate Analysis

Examine the relationship between each feature and the target variable (y, if included) to identify significant patterns or correlations.

Step 4: Outlier Detection

Identify and handle outliers in numeric columns such as balance, duration, and campaign that may skew the analysis.

**4. Modeling Process**

Step 1: Data Preprocessing

The dataset is cleaned by handling missing values, encoding categorical variables, and scaling numeric variables.

Step 2: Feature Selection

The features used for modeling include customer demographics, such as age, job type, marital status, education level, and financial status (balance, housing, loan). We exclude call-related features to focus on customer characteristics.

Step 3: Model Selection

Evaluated multiple classification algorithms, such as:

-> Logistic Regression: For a simple, interpretable baseline.

-> Decision Trees or Random Forests: For handling non-linear relationships and feature importance analysis.

-> Gradient Boosting Models (e.g., XGBoost, LightGBM, or CatBoost): For high accuracy and performance.

Used appropriate metrics to compare model performance, focusing on metrics like precision, recall, F1-score, and ROC-AUC to address class imbalance.

Step 4: Model Evaluation

Analyze the confusion matrix to understand the trade-offs between true positives, false positives, true negatives, and false negatives.

Step 5: Prediction

Using the trained clustering model, we predict the number of customers who are likely to subscribe and those who are not. Estimate potential reductions in call time by focusing only on high-potential customers.

**5. Clustering**

We apply K-Means and Hierarchical Clustering to identify clusters of customers with similar characteristics.

K-Means: Assigns customers to a predefined number of clusters based on customer attributes.

Hierarchical Clustering: Builds a tree of clusters based on customer similarity.


**6. Results**

--- > Initial Results Summary

**Modeling and Performance Insights**

After rigorous modeling, including sampling, hyperparameter tuning via Grid Search, and implementing ensemble techniques such as LightGBM Boosting, the model delivered strong results with an F2 score of 72%.
The F2 score emphasizes recall, aligning with the objective of minimizing missed opportunities (false negatives) and ensuring effective customer targeting.

**Call Reduction and Time Savings**

The model predicts non-subscribers (Class 0) with high accuracy, correctly identifying 9,408 true negatives, which is 24% of the total calls.
By avoiding these unnecessary calls, the company can save 39,827 minutes of call time, equating to significant cost and resource optimization.

**Time Savings and Efficiency**

With the model:

Total calls made = 6,622 calls.

Total time spent = 28,011 minutes (~467 hours).

Without the model:

Total calls made = 8,000 calls.

Total time spent = 33,840 minutes (~564 hours).

By using the model, the company reduces 5,829 calls, saving 17.2% of total call time (~97 hours).

**Missed Opportunities**

The model's predictions result in 10% of potential customers (Class 1) being classified as non-subscribers.
These missed customers could be revisited by identifying customer clusters or targeting specific segments for a secondary campaign, ensuring minimal loss in business impact.


---> Clustering Analysis: 

We found that different customer segments exhibit distinct behaviors. For instance, older customers with higher balances tend to fall into one cluster, while younger customers with lower balances form another group.

**K-Means Clustering**

![image](https://github.com/user-attachments/assets/e2730089-7f02-4c11-9f4a-f00afd856cad)


**Hierarchical Clustering**

![image](https://github.com/user-attachments/assets/e3ae9d61-6f96-4314-a894-e55eb4439da9)


**7. Requirements**

To run the project, you will need the following Python packages:

pandas

numpy

sklearn

matplotlib

seaborn

scipy

tableau (for visualizing the results)

**8. Conclusion**

Cluster 2 should be the primary focus, as these customers demonstrate the highest potential for conversion due to their financial stability, professional roles, and higher education levels.

Cluster 1 represents an aspirational group, offering opportunities to convert them with well-crafted financial products tailored to their mid-level income and career stage.

Marketing to Clusters 3 and 0 should be secondary, with efforts carefully aligned to their financial constraints and life stage.

**Business Implications**

By prioritizing high-value clusters (Cluster 2) and strategically targeting others (Cluster 1), the bank can maximize return on investment, reduce unnecessary outreach, and drive customer engagement effectively. This segmentation ensures marketing efforts are focused on segments with the greatest potential while optimizing resource allocation.






