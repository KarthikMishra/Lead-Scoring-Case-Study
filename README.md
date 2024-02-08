# Lead-Scoring-Case-Study
This case study aims to build a logistic regression model to predict the conversion chances of a marketing lead

# Problem Statement
The challenge at hand pertains to X Education, an esteemed online education provider catering to industry professionals.

Prospective learners often find their way to X Education's website, drawn by the allure of comprehensive online courses. The company strategically promotes its offerings across various digital platforms, including popular search engines like Google, ensuring maximum visibility.

Upon arrival at the website, visitors engage in various activities such as browsing courses, completing registration forms, or consuming informational videos. Those who furnish their contact details, be it email addresses or phone numbers, are identified as leads. Additionally, X Education receives leads through referrals from satisfied clients.

Once these leads are secured, the diligent sales team embarks on a proactive outreach campaign, reaching out through calls, emails, and other channels of communication.

However, despite these efforts, not all leads culminate in successful conversions. X Education experiences a typical lead conversion rate of approximately 30%.

Efforts are underway to optimize this conversion process, ensuring that a higher percentage of leads transition into enrolled learners, thereby maximizing the impact and reach of X Education's valuable courses.

# Business Goal:

X Education must identify the most prospective leads, namely those with the highest likelihood of converting into paying customers.

The company aims to develop a model that assigns a lead score to each lead, prioritizing those with higher scores for their increased likelihood of conversion. Conversely, leads with lower scores are expected to have a diminished likelihood of conversion.

The CEO has set a target lead conversion rate of approximately 80%, signaling the company's ambition to significantly enhance its conversion rates and optimize its sales efforts.

# Approach & Methodology

The following approach is followed to perform Lead Score Case study using Logistic Regression :

1. Understanding the data domain /Variables by referring to the Data Dictionary.

2. We have been given a Leads dataset to perform the analysis.

3. The analysis is performed by importing Leads dataset.

4. Data Cleaning is performed by analyzing(EDA) and then dropping the features that are not reliable. This is performed based on the following steps:

    - Handling the ‘select’ level that is present in many of the categorical variables by replacing with ‘NaN’ values
    - Dropping columns that are having high percentage of missing values by checking all the columns before dropping them
    - Dealing with the unique categories in the categorical features

5.  Data preparation is performed on the following steps:

    - Creating Dummy variables for categorical features
    - Perform train – test split (70 : 30)
    - Scaling the Numeric features using ‘StandardScaler’

6. Building Logistic Regression Model by performing the following techniques on Train data :

    - Initiating the first logistic Model Using the ‘GLM’ method of ‘statsmodel’ library
    - Automatic Feature Selection using RFE (Recursive Feature Elimination)
    - The model is being iterated until the features coefficients are significant based on the P-value < 0.05 and VIF < 5
7. Performing Evaluation metrices on the train data :

    - Confusion Matrix and Accuracy
    - Sensitivity and Specificity
    - Plotting ROC curve
    - Precision and Recall
8. Predicting on the Test data

9. Evaluation Metrices on the Test data

10. Lead Scoring is performed on the train and test data based on the probabilities obtained

# Conclusions

1. After Building the model, we have performed evaluation metrics on both train and test data. Checked based on the Sensitivity and Specificity as well as Precision and Recall. We have considered the optimal cutoff based on Sensitivity and Specificity for calculating the final predictions.
2. On the train dataset, for the optimal threshold of 0.3 we got the sensitivity or Recall as 91.65 % while the optimal cutoff chosen as 0.7 we got the sensitivity or Recall as 80.74 %.
3. On the test dataset, for the optimal threshold of 0.3 we got the sensitivity or Recall as 92.32 % while the optimal cutoff chosen as 0.7 we got the sensitivity or Recall as 80.42 %.
4. Also the lead score calculated shows the conversion rate on the final predicted model is above 80% in train and test set
5. The top 3 variables that contribute for lead getting converted in the model are
    - Tags_Lost to EINS – 6.6208
    - Tags_Closed by Horizzon – 6.0712
    - Tags_Will revert after reading the email – 4.4926
6. Based on the above summary of model prediction and evaluation it was concluded that this model seems to be good with good sensitivity or recall as satisfies our requirement.


