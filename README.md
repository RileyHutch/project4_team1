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




For our Random Forest model we used visualizations to analyze the multiple clusters used to group patients and features. In the below visualization we intially leveraged 5 clusters and used to the data to compare against models using 4 and 6 clusters.

![image](https://github.com/user-attachments/assets/36790475-af16-4a7f-b17d-65a0ef2e0a26)



	
## Machine Model Learning


### Random Forest

	• Identifying Clusters:
		○ We used clustering techniques to group patients based on their features. This helps in understanding the underlying patterns and similarities within the data.
		○ Clustering allows us to segment the patient population into distinct groups, which can be analyzed separately for more targeted insights.

	• Feature Importance Analysis:
		○ One of the key strengths of Random Forest is its ability to measure the importance of each feature in making predictions.
		○ By analyzing feature importance, we can identify which features have the most significant impact on the model's accuracy.
		○ This helps in understanding the key factors contributing to Alzheimer's diagnosis and can guide further research and interventions.

	• Insights from Feature Importance:
		○ The feature importance analysis revealed that cognitive and functional assessments, such as MMSE and Functional Assessment, are among the most impactful features for predicting Alzheimer's diagnosis.
 		○ This insight aligns with clinical knowledge and validates the importance of these assessments in detecting cognitive impairment.



### Keras Tuner 

	• Keras Tuner optimized our neural network by testing various architectures and hyperparameters, identifying an efficient model structure. This improved prediction accuracy while keeping the design 	streamlined for effective training.

### Neural Network

	• Our goal was to assess the impact of MMSE; mini-mental state examination, ADL; activities of daily living, and a functional assessment on model accuracy. By removing and reintroducing these features, we aimed to determine their significance and whether their exclusion would improve or hinder predictive performance.

 ### MRMR
 
	• mRMR (Minimum Redundancy Maximum Relevance) Selects the best features for machine learning by:
		○ Choosing features that strongly predict the target (maximum relevance)
		○ Avoiding features that are too similar/repetitive (min redundancy) 
  		○ It does this by calculating a similarity score


## Tech Stack
You will need to follow these steps if you're cloning the repository for your own exploration. First, open a command-line interface. Follow the instructions to set up a [Conda environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) and activate your new environment. Then install all the python libraries we used in the project by typing: 
```
pip install -r requirements.txt
```

## Resources

	Dataset: https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset
 	mrmr: https://github.com/smazzanti/mrmr

## Conclusion and Summary

### Summary

The integration of the Mini-Mental State Examination Score, Activities of Daily Living Score, and Functional Assessment significantly enhanced the accuracy of the model. To further optimize performance, Keras Tuner and the Minimum Redundancy Maximum Relevance (MRMR) technique were employed to identify key features and refine the model design, resulting in more impactful predictions. With these cognitive assessments included, the model achieved an impressive 85% accuracy. In contrast, accuracy ranged from 68% to 74% without them. Moving forward, incorporating additional factors such as genetic data and specific lifestyle elements could further elevate the model’s predictive power and overall accuracy.

### Considerations

Although we were able to reach over 80% accuracy with the included cognative assessments from the dataset, our team considered additonal data relevant to postive diagnosis that could allow for additonal optimization and improvment without the cognative assessments. Access to the below data and patient information would could improve and expand the model's capabilty. 

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
	
