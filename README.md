# Logistic_Regression_Analysis
Based on a dataset from the Kaggle website(https://www.kaggle.com/datasets/thedevastator/cancer-patients-and-air-pollution-a-new-link), this project aims to investigate the correlation between age, alcohol use, air pollution, and the level of chronic lung disease of patients.
# Dataset
I choose the dataset from the Kaggle website (https://www.kaggle.com/datasets/thedevastator/cancer-patients-and-air-pollution-a-new-link), uploaded and updated by THE DEVASTATOR. The dataset contains information on patients with lung cancer, including their age, alcohol use, etc. This dataset includes 26 variables, such as Chest.Pain, Frequent.Cold, Gender, Dry.Cough, etc., and 1000 observations. In this case, it provides insights into the correlation between variables like Chest.Pain and conditions of lung cancer.
# Research Question & motivation
My research aims to investigate the correlation between age, alcohol use, air pollution, and the level of chronic lung disease of patients. The independent variables are age ("Age"), alcohol use ("Alcohol use"), smoking ("Smoking"), and air pollution ("Air Pollution"), and the dependent variable is the levels of chronic lung cancer ("Level"). Ideally, I think variables like genetics and occupational exposure will be helpful for predicting my dependet variable.

I hypothesize that there is a positive correlation between age, smoking, alcohol use, air pollution, and the severity of chronic lung cancers. In other words, I hypothesize that for people who are older, or smoke, or consume more alcohol use, or live in places with more severe air pollution, they will be more likely to have severe chronic lung cancers. My motivation for this research is to better know about factors contributing to lung cancer and have more accurate predictions toward the occurrence of chronic lung cancers.
 
My dependent variable ("Level") is categorical, from 0 to 7. Therefore, for my research, I would cut off the levels of chronic lung diseases into "low severity" and "high severity" to make it a binary variable, which would be suitable for the logistic regression. Also, as my dependent variable is countable (from 1 to 7), a Poisson regression will also be appropriate for it.

# Variables of Interest
- Age: The age of the patient. (Numeric) It has a median at 36, min at 14, max at 73. 
- Air Pollution: The level of air pollution exposure of the patient. (Categorical) It has a median at 3, min at 1, max at 7.
- Alcohol use: The level of alcohol use of the patient. (Categorical) It has a median at 5, min at 1, max at 7.
- Smoking: The level of smoking of the patient. (Categorical) It has a median at 3, min at 1, max at 8.
- chronic Lung Disease: The level of chronic lung disease of the patient. (Categorical) It has a median at 4, min at 1, max at 7.

# Interpretations
For the logistic regression, the statistic table shows that all of the variables (Age, Alcohol.use, Air.Pollution, Smoking) are positively correlated with the severity of chronic lung cancer, as the log odds of them are positive. At the same time, there's a statistically significant correlation between Age and chronic.Lung.Disease (p<0.001), and between Alcohol.use and chronic.Lung.Disease (p<0.001), and between Air.Pollution and chronic.Lung.Disease (p<0.01), and between Smoking and chronic.Lung.Disease (p<0.001). 

According to the odd ratios, for every one unit increase in Smoking, it's 76.4% more likely (log ratio = 1.7638) to have severe chronic lung diseases (when chronic.Lung.Disease=1). For every one unit increase in Air.Pollution, it's 22.1% more likely (log ratio = 1.2211) to have severe chronic lung diseases. For every one unit increase in Age, it's 3.5% more likely (log ratio = 1.0354) to have severe chronic lung diseases. For every one unit increase in Alcohol.use, it's 90.5% more likely (log ratio = 1.90529) to have severe chronic lung diseases. In this case, Alcohol.use has the strongest correlation with the severity of chronic lung diseases. This conclusion can also be reflected by the logistic regression plot. Compared to other variables, we can see a more clear positive correlation between Alcohol.use and chronic.Lung.Disease. 

According to the Poisson model, while it indicates positive correlations between all these variables and the severity of chronic lung cancer (chronic.Lung.Disease), only the correlations between Smoking and chronic.Lung.Disease and and between Alcohol.use and chronic.Lung.Disease are statistically significant (p<0.001). 

According to the Residuals vs. Fitted plot, the residuals do roughly form a “horizontal band” around the 0 line, indicating that the assumption of homoscedasticity is met. For the QQ plot, the points generally fit the straight line, indicating that the assumption of normal distributed residuals is met. Furthermore, I think the model fit well, as the ratio is 0.3727, which is close to 1 (expect it to be 1 if it’s a good fit) and the chi-square test is 1 that shows it’s a good fit. The high p value (p=1) in the overdispersion test does not reject the null hypothesis that the model do not have overdispersion, indicating that the model is a good fit and doesn't have overdispersion.

In conclusion, the results show valid correlations between variables of Alcohol.use and Smoking and chronic.Lung.Disease. Variables of Age and Air.Pollution only have very minor correlation with chronic.Lung.Disease, and may not be statistically significant. In this case, my hypothesis is only partially correct—there are only positive correlations between Alcohol.use and Smoking and chronic.Lung.Disease. For future analysis, I think some other variables can be taken into consideration, such as gender, weight, gene, etc. In this case, the prediction of the severity of chronic lung diseases can be more accurate and precise through future studies.

<img width="481" alt="image" src="https://github.com/SophieJiaBo/Logistic_Regression_Analysis/assets/168926944/d4a684d3-4a2a-41ce-9826-9baade4ac5db">
<img width="499" alt="image" src="https://github.com/SophieJiaBo/Logistic_Regression_Analysis/assets/168926944/22f74a02-0298-4cc9-8db7-d6b569c5d81b">
<img width="482" alt="image" src="https://github.com/SophieJiaBo/Logistic_Regression_Analysis/assets/168926944/33683458-0b54-492b-9d4b-6a9e3f9246ea">
