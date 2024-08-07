# Custom Named Entity Recognition (NER) for Healthcare Data
>This repository contains a custom Named Entity Recognition (NER) model designed to extract diseases and their corresponding treatments from medical text data. The model is tailored for a health tech company called ‘BeHealthy’.

## Introduction:
This project focuses on processing and analyzing medical text data to identify diseases and treatments using Named Entity Recognition (NER). The project involves text processing steps, feature creation, and model building.

## Steps to Approach:
#### 1. Data Preprocessing
- Construct sentences from individual words in train_sent and test_sent.
- Construct sequences of labels from train_label and test_label.
  
#### 2. Concept Identification
- Use PoS tagging to identify and count NOUN and PROPN tags.
- Print the top 25 most frequent NOUN and PROPN tokens.
 
#### 3. Defining Features for CRF
- Include PoS tags and preceding word information as features.
- Mark the beginning and end of sentences in the feature set.
  
#### 4. Getting Features and Labels of Sentences
- Extract feature values for each sentence.
- Extract label sequences for each sentence.
  
#### 5. Defining Input and Target Variables
- Extract features as input variables for the CRF model.
- Extract labels as target variables for the CRF model.
  
#### 6. Building the Model
- Train a CRF model using the features and target variables.
  
#### 7. Evaluating the Model
- Predict labels for the test dataset.
- Calculate the f1 score using actual and predicted labels.
  
#### 8. Identifying Diseases and Predicted Treatments
- Create a dictionary mapping diseases to predicted treatments.
- Predict the treatment for a specific disease (e.g., 'hereditary retinoblastoma').
  
## Problem Statement:
The goal is to develop a custom NER model to extract disease names and their treatments from medical text data. The output should be a structured format (e.g., dictionary or table) listing diseases and their probable treatments.

## Dataset:
The datasets provided for this project are:

train_sent: Training sentences.
test_sent: Testing sentences.
train_label: Training labels.
test_label: Testing labels.

## Technologies Used:
- Python 3.6 or higher
- Libraries: `pandas`, `sklearn`, `sklearn-crfsuite`, `nltk`, `numpy`

## Results:
The results, including the dictionary of diseases and treatments, can be found in the results directory.

## Contact:
-Created by www.linkedin.com/in/ritik-kumar-717313221 - feel free to contact me!
