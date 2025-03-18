# Project 4 - Predicting Alzheimer's Disease with Machine Learning

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

For intial review of the dataset, we used Matplotlib to create visualizations to analyze patient counts against each of the features. In the following visualization we used patient counts to compare the various symptoms accounted by patients.

![image](https://github.com/user-attachments/assets/e278518f-5f70-4591-bcf2-82e2c0ecc38c)

For intial review of the dataset, we used Matplotlib to create visualizations to analyze patient counts against each of the features. In the above visualization we used patient counts to compare the various symptoms accounted by patients. 

![image](https://github.com/user-attachments/assets/36790475-af16-4a7f-b17d-65a0ef2e0a26)


	
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
You will need to follow these steps if you're cloning the repository for your own exploration. First, open a command-line interface. Follow the instructions to set up a [Conda environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) and activate your new environment. Then install all the python libraries we used in the project by typing: 
```
pip install -r requirements.txt
```

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
	
