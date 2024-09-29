# Med_Home_Adherence
Evaluating member adherence to utilizing a medical home and future propensity scoring

Overview of the expanded solution for evaluating member adherence to utilizing a medical home (assigned PCP) and creating propensity scores for future adherence:
1. Data Structure: The solution begins by creating a dataset with relevant features such as age, gender, chronic conditions, health plan type, tenure, and recent PCP visit history. Each member's adherence to their assigned PCP is tracked.
2. Independent Feature Propensity Scores: Using a logistic regression model, the script calculates a propensity score for each feature (age, gender, chronic condition, etc.), representing the likelihood of adherence based solely on that feature.
3. Feature Weighting: The contribution of each feature to the final score is weighted according to its importance, derived from the logistic regression model coefficients. These weights ensure that features with more predictive power have a greater impact on the overall propensity score.
4. Final Propensity Score Calculation: The final propensity score is a weighted sum of the independent feature scores. This score indicates the overall likelihood that a member will continue utilizing their medical home effectively.
5. Risk Identification and Outreach: Members with a propensity score below a predetermined threshold (e.g., 0.5) are flagged as high risk for non-adherence. The script generates an outreach report identifying these members, allowing for proactive intervention.
6. Continuous Monitoring: The model can be updated regularly as new data comes in, allowing for continuous evaluation of member behavior and updating of propensity scores.

The solution attempts to predict future behavior, evaluates it through multiple data elements, and generates actionable insights to help ensure member adherence to their assigned PCPs, which is critical for maintaining effective care within a medical home model. This would be paired with a report on members accessing care outside of their medical home. Those cases may need to be further addressed in the model training criteria.
