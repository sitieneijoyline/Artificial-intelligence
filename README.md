AI for HumanForYou: Employee Attrition Prediction

Overview

This project, titled AI for HumanForYou, focuses on predicting employee attrition using machine learning techniques. By analyzing 2015 employee in-and-out time data alongside general and survey data, the project aims to identify key factors influencing employee turnover and provide actionable insights for HR decision-making. The predictive models used include Random Forest, Support Vector Machine (SVM), and Elastic-Net Logistic Regression, optimized with GridSearchCV.

Group Members:





CHERIBET DROUICHE Abderaouf



CHEPKOECH Joyline



LUNEL Alexis

Project Objectives





Clean and preprocess employee in-and-out time data, general employee information, and survey data.



Calculate average daily worked hours for each employee.



Merge datasets to create a comprehensive dataset for analysis.



Train and evaluate three machine learning models to predict employee attrition.



Identify key predictors of attrition, such as worked hours and job satisfaction.



Provide a scalable framework for workforce analytics to support HR strategies.

Dataset

The dataset comprises the following files:





general_data.csv: Contains demographic and employment details of employees (e.g., age, department, years at company).



employee_survey_data.csv: Includes employee survey responses (e.g., job satisfaction, work-life balance).



manager_survey_data.csv: Contains manager survey responses (e.g., job involvement, performance rating).



in_time.csv: Records employee check-in timestamps for 2015.



out_time.csv: Records employee check-out timestamps for 2015.

Data Preprocessing





Loading Data: Loaded all datasets using pandas.



Cleaning: Removed columns with all NaN values from in_time and out_time datasets.



Timestamp Conversion: Converted in_time and out_time timestamps to datetime format for accurate calculations.



Worked Hours Calculation: Computed daily worked hours by subtracting check-in from check-out times and calculated the average daily worked hours per employee.



Merging: Combined all datasets on EmployeeID using a left join to create a final dataset for modeling.

Methodology

Three machine learning models were employed to predict employee attrition:





Random Forest Classifier: A tree-based ensemble model optimized for high precision.



Support Vector Machine (SVM): A model effective for binary classification tasks, tuned for optimal performance.



Elastic-Net Logistic Regression: A regularized logistic regression model balancing L1 and L2 penalties.

Model Optimization





GridSearchCV: Used to fine-tune hyperparameters for each model to maximize performance.



Evaluation Metrics: Models were evaluated using accuracy, precision, recall, F1-score, and AUC-ROC.

Key Findings





Key Predictors: Worked hours and job satisfaction were significant predictors of attrition.



Model Performance:





Random Forest: Highest accuracy (88.21%), precision (94.55%), and F1-score (44.27%).



SVM: Highest AUC-ROC (0.9000), but lowest recall (19.70%).



Elastic-Net: Moderate performance with an AUC-ROC of 0.7647.



Conclusion: Random Forest was the best-performing model due to its high precision and balanced F1-score, making it suitable for minimizing false positives in attrition predictions.


Installation and Setup

To run the project locally, follow these steps:





Clone the Repository:

git clone https://github.com/your-username/AI-for-HumanForYou.git
cd AI-for-HumanForYou



Install Dependencies: Ensure Python 3.12+ is installed. Install required packages using:

pip install pandas numpy scikit-learn matplotlib



Run the Notebook: Open the Jupyter Notebook (Deliverable_Group4_AI_for_HumanForYou (1).ipynb) in Jupyter Lab or Jupyter Notebook:

jupyter notebook

Results





Random Forest excelled in precision (94.55%) and F1-score (44.27%), making it ideal for identifying employees at risk of attrition with minimal false positives.



SVM showed the highest AUC-ROC (0.9000), indicating strong class separation but lower recall.



Elastic-Net Logistic Regression had the lowest performance across most metrics but still provided useful insights.



The project highlights the importance of worked hours and job satisfaction in predicting attrition, offering HR teams a data-driven tool for retention strategies.

Future Work





Explore additional features, such as employee engagement metrics or external factors (e.g., market conditions).



Implement advanced models like Gradient Boosting or Neural Networks for improved performance.



Deploy the model as an API for real-time attrition predictions.

Acknowledgments

This project was completed as part of a group effort for [Course/Organization Name]. We thank our instructors and peers for their guidance and feedback.
