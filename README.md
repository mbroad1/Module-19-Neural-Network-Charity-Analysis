# Module 19 Challenge: Neural Network Charity Analysis

## Purpose:
The purpose of this analysis is to evaluate which non-profit organizations should receive funding from another non-profit organization, Alphabet Soup Charity, which allocates funds to different non-profits annually. In order to determine which non-profit organizations should receive funding, I created a deep learning neural network that evaluated the success of previous non-profit organizations that received funding based on several factors like the type of application they submitted and the purpose of the funding as the inputs to the neural network. After creating the neural network, I did my best to optimize it in order to increase its accuracy in determining which non-profit organizations would be successful in utilizing the funding effectively.
---

## Results:

### Data Preprocessing
#### Targets and Features:
![Targets_and_Features](https://github.com/mbroad1/Module-19-Neural-Network-Charity-Analysis/blob/main/target%20and%20features.png)
- The target, y, was assigned to the column "IS_SUCCESSFUL" which assigned a 1 to organizations that were successful in utilizing the donated funds effectively and a 0 to organizations that failed to use the funds wisely.
- The features (denoted all as X) were all the other variables that were not "IS_SUCCESSFUL", "EIN", and "NAME" such as "APPLICATION_TYPE" and "USE_CASE" because these inputs may be helpful in determining the relationships between the variables and how those relationships influence the success or failure of an organization to use the donated funds well.
