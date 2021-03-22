# Research - A Novel Heuristic Method to Improve Employee Retention Using Machine Learning

## Ideas
- Tradeoff between attrition rate and cost to company ?
## Goals
- Create a good classifier to predict the attrition of an employee correctly
- Use the classifier to help the company prevent further attrition by making necessary changes by using reverse modelling

## Current Progress
- Created a stack ensembled classifier with a F1 score of 0.608 on test set and 0.78 on train set. Taking into account the lack of training examples ( about 1200 ) this is considerably a good score

## To do
- Identify Slack variables
- Creating priority between them
- Using the ω ( willingness factor ) and the features that have "give" ( Decided by the employer as well ) find the best possible combination of changes that the employer can make to prevent attrition

## Inputs 
- Company to decide on the willingness factor ( ω ) to change the variable on a scale of ( 0 - 100), which will be normalized so that all factors add up 

## Output
- Various possible changes will be found using the classifier, the one with the lowest change (least cost to the Employer) required will be the best possible solution
- Best possible solution for the Employer to increase their retentive power

## Notes
##An important thing to note -> 
- The unavailabilty of adequete amount of data has resulted in the F1_score above, we reckon, given a large enough dataset, employee attrition could be predicted (not as a judge but a guide) with an F1_score of 0.97.
- For the record it must also be stated that the dataset which was used to train the model above was an imbalanced dataset with only 6.7% attrition in the whole dataset
- **We use the reverse modelling step to take the interests of the company into account too**

##Definitions
- _F1_score_ -> F-score or F-measure is a measure of a test's accuracy. It is calculated from the precision and recall of the test.
- _Precision_ -> It's the number of true positive results divided by the number of all positive results, including those not identified correctly.
- _Recall_ -> It's the number of true positive results divided by the number of all samples that should have been identified as positive


![image](https://user-images.githubusercontent.com/46497726/111865493-55ee3280-898d-11eb-84d5-5a23f5d6a70d.png)


- _ω ( willingness factor )_ -> A factor to find the best possible change
- _Imbalanced dataset_ -> One set of classes dominate over another set of classes. It causes the machine learning model to be more biased towards majority class. It causes poor classification of minority classes.

The minimization goal is 
- <img src="https://latex.codecogs.com/png.latex?\inline&space;min_{for-all-possible-solutions}[\sum_{x&space;\,\varepsilon&space;\,slackvariables&space;}^{}(1-\omega_{x})*\Delta&space;x]" title="min_{for-all-possible-solutions}[\sum_{x \,\varepsilon \,slackvariables }^{}(1-\omega_{x})*\Delta x]" />

The dataset used for this research can be found [here](https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset)

![image](https://user-images.githubusercontent.com/47801727/111938656-7aaeeb00-8af0-11eb-8928-4b17a48775fe.png)
