**WINE QUALITY PREDICTION - Building Deep Learning Models in Python With Keras**


## Project aims:
This project is about predicting the Wine quality by applying Neural Network - a deep learning technique. 

The main aims of the project is to create a AI system that can predict the quality of a wine. In order to do that, first, I will get the data provided by customer in the folder "additional_resources/datasets/Wine Quality/wine.csv"; 

![Picture (Image)](https://www.wine-searcher.com/images/news/74/12/faves1-10007412.jpg)

Then, I will explore and clean the data (no missing values). 
After that, I will define the problems as its classification or regression problems.

So the main target is to build a neural network model that can predict the quality of wine (i.e. good or bad). Then, improving the model performance by tuning hyperparameters.

## Installation
### Python version
* Python 3.8

### Packages used
* pandas==1.3.2
* scikit-learn==0.24.2
* matplotlib==3.3.3
* tensorflow==2.6.0
* plotly==4.14.1


## **The steps to build a baseline model using Keras**
1. Load Data.
2. Define Keras Model.
3. Compile Keras Model.
4. Fit Keras Model.
5. Evaluate Keras Model.
6. Tie It All Together.
7. Make Predictions

## 1. Data description:
  + **Features** (input variables):
  
      1 - fixed acidity  
      2 - volatile acidity       
      3 - citric acid       
      4 - residual sugar       
      5 - chlorides      
      6 - free sulfur dioxide       
      7 - total sulfur dioxide       
      8 - density       
      9 - pH      
      10 - sulphates      
      11 - alcohol
      
  ![Data description](./assets/data_description.jpg)    
  ### **Inferences from the dataset**:

   * The average of **'quality'** is 5.81 
   * **pH** has a high mean of 3.21, max is 4.01
   * **alcohol** has also high mean 10.49


  + **Target** (output variable): 
      quality: score between 0 and 10
      
 <img src="assets/target_distribution.jpg" width="400">
 
The rating of wine quality distribute is mostly at 5, 6, 7. There is an imbalance in data distribution between categories. 

  ### Binary classifier

| original quality values            | binary quality value         |
|-------------------|----------------------------------------------|
| 1 - 5 | 0 (bad)                         |
| 6 - 9 | 1 (good) | 

   <img src="assets/target_binary.jpg" width="400">

  + **Correlation between variables**
   <img src="assets/heatmap.jpg" width="500">

+ **Inferences from the heatmap**:
    * High degree of positive correlation between **alcohol** and **quality**. Wines with high alcohol content are perceived as better quality
    * Negative correlation between **quality** and **density**, **volatile acidity**.F

    * Features have positive impact on Wine Quality are: 'fixed_acidity', 'residual_sugar','free_sulfur_dioxide', 'pH', 'sulphates', 'alcohol'
    * Features have negative impact on Wine Quality are: 'volatile_acidity', 'citric_acid', 'chlorides', 'total_sulfur_dioxide', 'density'


## Building a basic neural network  model

<img src="assets/basic_NN_model.jpg" width="500">



<img src="assets/base_plot_acc_loss.jpg" width="600">
  + Model evaluation:
 
    - the Test set - loss: 0.4942 - accuracy: 0.7610   
    - the Training set -loss: 0.4418 - accuracy: 0.7983

<img src="assets/base_confusion_matrix.jpg" width="400">

## Turning Models

  + Tuning on Activation functions

  + Tuning on Optimizer functions

<img src="assets/base_confusion_matrix.jpg" width="400">

## Grid search


### Root folder
| File            | Description                                                 |
|-------------------|-------------------------------------------------------------|
| assets/wine_full.csv| Directory containing graphics                        |
| DL-wine-quality | Python script containing functions for dataset manipulation|
| GridSearch_HyperParameters | Python script containing functions for Gridsearch code | 
| main.py          | Python script with the final version of the project | 


# Contributor
| Name                   | Github                              |
|------------------------|-------------------------------------|
| Minh Hien Vo | https://github.com/minhhienvo368  |


# Timeline
07/09/2021 - 09/09/2021
