

(2) This project compares 2 architectures for facial beauty evaludation based on SCUT-FBP5500 dataset: traditional Convolutional Neural Networks along with a novel approach: transfer learning with Vision Transformer fine-tuned on this task. The results can be found in ISODS-Facial Beauty Evaluation pdf file. This repo also adopts another pdf file written by the author for Object Detection in Videos


# Facial Beauty Evaluation Project 
### Aim:
This project's goal is to rate the score of a face in range from 1 to 5 (5 is the most attractive) such that the predicted score is closest to a set of pre-defined labels/response variable. This project applies transfer learning by utilizing pretrained models on Facial Recognition tasks and fine-tunes them on our task - facial beauty evaluation. For this project, I use pretrained Vision Transformer and benchmarked this against other traditional CNN architectures such as Res-net 50 and achieves SOTA performance on this task. I also deployed ElasticViT, a transformer-based architecture, on a software designed by our team (ISODS) such that this product could be integrated within an app and be applied in the real world.

### Author:
* Ngoc Duy Tran: ngocduyt@student.unimelb.edu.au

# Structure of Directory
    .  
    ├── SCUT-FBP5500 
    │   ├── data  
    │   │   ├── curated  
    │   │   ├── landing  
    │   │   └── raw   
    │   ├── notebooks   
    │   │   └── epoch_VIT.ipynb
    │   │   └── traditional_CNN.ipynb 
    │   ├── report  
    │   │   └── paper.pdf 
    │   ├── README.md  
    └──  

# Pipeline
In order to replicate the files, visualisations, models, etc. produced throughout this project, the following actions should be executed in the order as outlined below. 

## 1. DOWNLOADING DATA

The data has already been downloaded and zipped to the data directory under landing layer.

Folder "Images" contains 5500 frontal, unoccluded faces aged from 15 to 60 with neutral expression. It can be divided into four subsets with different races and gender, including 2000 Asian females, 2000 Asian males, 750 Caucasian females and 750 Caucasian males.

## 2. PREPROCESSING

The data has been preprocessed; however, due to copyright reasons from the team, these are not included here. However, the data has been pre-processed and partitioned into training and testing set (60: 40) or five-fold cross validation, depending on purposes. These are all saved under the curated layer: `data/curated/train_test_files` directory

## 3. MODELLING
- Run `notebooks/epoch_VIT.ipynb`: this notebook implements the Vision Transformer architecture. This adopts transfer learning by fine-tuning this model based on pre-trained model on facial recognition
- Run `notebooks/traditional_CNN.ipynb`: this notebook implements CNN-based architectures such as Res-net34/50, VGG16 pretrained on facial datasets. 

## 4. ANALYSIS AND REPORT
- The paper is located under `report/ISODS- Facial Beauty Prediction with Vision Transformer - REVISED.pdf`. 


# NOTES
- The full project link could not be provided as it's part of the organization's code and could not be shared externally. However, under the agreement of International Society of Data Scientists, I am only allowed to share the pre-alpha version of the model implementation code (earliest version) on my personal github.


# CONTACT
- Should you have any questions for this repo, please contact me via the email above.



