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

![image](https://github.com/user-attachments/assets/e278518f-5f70-4591-bcf2-82e2c0ecc38c)


![image](https://github.com/user-attachments/assets/36790475-af16-4a7f-b17d-65a0ef2e0a26)


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

## Tech Stack

## Resources

	Dataset: https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset
 	mrmr: https://github.com/smazzanti/mrmr

## Conclusion and Summary

### Considerations

Although we were able to reach over 90% accuracy with the included cognative assessments from the dataset, our team considered additonal data relevant to postive diagnosis that could allow for additonal optimization and improvment without the cognative assessments. Access to the below data and patient information would could improve and expand the model's capabilty. 

	• Genetic Features:
		○ APOE ε4 Genotype (Carrier vs. Non-Carrier)
		○ Other Genetic Markers (Polygenic Risk Score, CLU, PICALM, BIN1, TREM2)
	• Imaging-Based Features:
		○ Structural MRI Measures (Hippocampal Volume, Entorhinal Cortex Thickness, Cortical Atrophy Pattern, Whole-Brain Atrophy)
		○ White Matter Lesions (WMH Volume, Fazekas Score)
		○ FDG-PET Metabolic Activity (Regional Metabolic Values, AD-Pattern Hypometabolism Score)
		○ Amyloid PET (Amyloid PET Status, SUVR)
		○ Tau PET (ROI SUVR, Braak-Stage Estimate)
		○ Diffusion Tensor MRI (DTI)
		○ Functional MRI (fMRI) / Resting-State Connectivity
		○ Retinal Imaging/Ocular Tests
		○ EEG/Magnetoencephalography
	• Lifestyle and Environmental Features
		○ Midlife Obesity (BMI)
		○ Late-Life Underweight
		○ Social Engagement (Living Alone, Social Activity Frequency)
		○ Mental Stimulation (Hobbies, Learning Activities)
		○ Hearing Loss
	• Clinical Data
		○ MoCA (Montreal Cognitive Assessment)
		○ Delayed Word Recall ( or other specific memory tests)
		○ FAQ (Functional Activities Questionnaire)
		○ Anxiety
		○ Irritability
	
