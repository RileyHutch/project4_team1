# Project 4 

## Team 1
  	Riley Hutchinson,
 	 Quinn Jones,
 	 Jim Cockerham,
 	 Katrina Rodriguez,

## Project Proposal
The aim of our project is to assess the predictability of Alzheimer's disease diagnosis, enabling early intervention strategies. We will analyze the relationship between patient demographic information and lifestyle factors to identify trends in positive diagnoses using binary prediction models. 

These are the questions we used to create our data analysis, visualizations, and models:

    • Can we create a model to predict an Alzheimer's diagnosis with 90% or more accuracy?
        ○ What features are most impactful for increased accuracy? 
        ○ What features were least relevant to the model's accuracy?
        ○ What is the best type of model to optimize accuracy?
        ○ What other information or dataset would be impactful to the learning model?


## Data Analysis
For our project, we utilized a comprehensive dataset from Kaggle, which includes detailed health information for 2,149 patients. Each patient is uniquely identified with IDs ranging from 4751 to 6900. The dataset encompasses demographic details, lifestyle factors, medical history, clinical measurements, cognitive and functional assessments, symptoms, and Alzheimer's Disease diagnoses.

During initial preprocessing, we discovered that all values in the dataset are non-null and numerical, and there are no duplicate records. We agreed to initially drop the DoctorInCharge and PatientID columns, and allowing us to leverage the remaining 33 columns.


## Data Visualizations

Below are some of the data visualizations we used to review and compare the features from our dataset.

	• Determining which data was impactful to accuracy scores
	• Cognitive and Functional Assessments Impact to Data
		• MMSE: Mini-Mental State Examination score, ranging from 0 to 30. Lower scores indicate cognitive impairment.
		• FunctionalAssessment: Functional assessment score, ranging from 0 to 10. Lower scores indicate greater impairment.
		• MemoryComplaints: Presence of memory complaints, where 0 indicates No and 1 indicates Yes.
		• BehavioralProblems: Presence of behavioral problems, where 0 indicates No and 1 indicates Yes.
		• ADL: Activities of Daily Living score, ranging from 0 to 10. Lower scores indicate greater impairment.
	• Contributed to high accuracy of positive diagnosis due to assessments specifically designated to detect Alzheimer's.
	• What is the impact of dropping the cognitive assessments from the model and comparing accuracy since these are tests specifically targeted for diagnosis?
	
## Machine Model Learning
	• Random Forest- 
		○ Jim Accuracy .98 with cognitive assessment, without cognitive assessment .50, optimization .68
		○ Quinn Random Forest 95,
		○ Take away narrowed down important features that contributed to accuracy
	• Keras Tuner -
		○ Without any cognitive assessments accuracy of  66.5
	• Neural Network - 
		○ dropping cognitive assessments 66 (2 hidden layers few neurons)
		○ Optimization with additional neurons (
	• MRMR
		○ Keras Tuner -
		○ Neural Network- increased features accuracy dropped, 

## Conclusion and Summary

### Considerations

## Tech Stack

## Resources

https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset
