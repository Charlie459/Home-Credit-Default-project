

# Home-Credit-Default-project

Summary of business problem and project objective:

Individuals with poor or nonexistent credit face significant challenges in obtaining personal, home, or business loans. Those seeking loans often fall victim to lenders who impose excessively high fees and annual interest rates.

Home Credit aims to address this issue by tailoring its business approach towards individuals with limited or unfavorable credit histories, while avoiding predatory lending tactics. To achieve this goal, Home Credit must devise a method to assess the repayment capability of each loan applicant.

In this project, I will analyze the 'application_train' dataset provided by Home Credit and utilize Random Forest algorithm to predict which customers are more likely to encounter difficulties in repaying their loans. Through classification techniques, my objective is to develop a model with high accuracy and ROC-AUC scores to identify customers prone to payment issues.

Group solution to the business problem:

To help solve this Kaggle project I collaborated with other students to develop various predictive models to see which could produce the best results. My group discovered that the XGBoost model, a gradient-boosting decision tree returned the best kaggle score of .75.

My contribution to the project:

I researched various predictive modelling techniques to find which would be the best to use in this scenario. I came across ensemble learning, which aggreates multiple weak models into a strong model. These models reduce prediction variance and can often perform well with imbalanced data. Random forest, bagging and boosting are all varieties of ensemble models. I decided that XGboost would be the best for this data as it can train models on the residuals made by previous models. While it can take awhile to run given the number of epochs, the dataset wasn't too large for this to be an issue.

The business value of the solution:

Because misclassifying no default is much more costly than misclassifying default, it is important for the company to have faith that the model can handle risk in a controllable manner. We could set a threshold for exactly how much more costly predicting default is than no default and input this information into the model. This kind of manipulation for each scenario makes the XGBoost model make strong reliable predictions but also can be tailored to the specific cost/benefit of this particular company.

Difficulties encountered along the way:

Because the data has a large majority class, meaning the number of individuals who did not default is much higher than those who do default, we needed to find a model that could handle high class imbalance. Many models we had learned about in class would produce high accuracy, but this was misleading as simply predicting the majority class each time would result in a 92% accuracy. We could simply over-sample the minority class but creating synthetic observations to equal the amount in the majority class can be dangerous as it leads to more false positives.

What I learned in the project:

Each dataset has unique characteristics that must be accounted for to achieve the desireable accuracy. Models that work for some data will not do well in other scenarios, in this case it was a highly imbalanced majority class. Simply predicting the majority class would give a high accuracy but result in high cost for the company, so it was very important to find error metrics that could accurately represent the risk and true accuracy. Also, being able to upload the model to Kaggle to confirm the predictive power gives more confidence that the model does well with new data.
