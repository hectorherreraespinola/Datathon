
## <h1> **Autor: HECTOR JAVIER HERRERA ESPINOLA** </h1>

## Last updated 12/02/2023<hr>  

### <h1 align="center">**`MACHINE LEARNING ON HOSPITALIZATIONS`**</h1>


## **Objetive**
The project consist in loading a dataset on hospitalizations. By exploring and training a Machine Learning Model, it is needed to predict if patients will spend more than 8 days in hospital, training it with the part of the dataset that has the results, and using that as a reference for the other part that doesn't. 


### Context
To know if a patient will have a prolonged stay is very important for the operation of the hospital/clinic. For this work, a dataset that was divided was used, and one part did not have the hospitalization time.

<p align="center"> <img alt="ML" src="https://ml2analytics.files.wordpress.com/2020/04/digits-dataset-scikit-learn-machine-learning-python-tutorial.png" height=200px> 

### Tech stack
* [Python](https://docs.python.org/3/)
    * [Pandas](https://pandas.pydata.org/)
    * [Numpy](https://numpy.org)
    * [sklearn](https://scikit-learn.org/stable/index.html)  
    * [Seaborn](https://seaborn.pydata.org)
    * [Matplotlib](https://matplotlib.org)

<hr>

## Workplan:
1. EDA (Exploratory data analysis)
2. Data preprocessing
3. Correlation analysis
4. Features treatment
5. Pipeline
6. Model creation
7. Prediction

### Repository archives
- [**Datasets**:](./Datasets/) Inside this folder are the raw files used to carry out the project, and also the file that was created with the results of the prediction. The name of this one matches the GitHub user.
- [**Mejor_pipeline**:](./Mejor_pipeline.pkl) The pipeline with the best accuracy is saved in this file, to avoid running all the training sessions again.
- [**Modelado**:](./Modelado.ipynb) Notebook where the work is done.


## EDA <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width=40px height=40px/><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original-wordmark.svg" width=40px height=40px/><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width=40px height=40px/>
For the first step, the EDA is performed. The datasets were explored, reviewing data types and missing data. Based on this analysis, some initial conclusions are drawn.

## Data preprocessing
Because the relevant feature is a categorical variable, the numerical correlation analysis is useless, so statistical analysis is used.

## Correlation analysis
With Python libraries, the P value of the categorical variables is obtained, to evaluate the correlation.

## Features treatment
Irrelevant features are removed, and recategorization is performed using OrdinalEncoder and OneHotEncoder.

## Pipeline
Pipeline is used to train multiple models, and to be able to evaluate which one provides the best precision. As it is a process that takes a long time, we save the result in a file to import it later.

## Model creation
The decision tree model is selected, according to the Pipeline result. Using Cross Validate and a loop, the optimal depth of the tree is obtained. The model is trained with train_test_split. Then, we compare the results obtained with the one evaluated in the Pipeline, and we keep the most balanced.
<p align="center"> <img src="https://static.vecteezy.com/system/resources/previews/001/234/042/original/decision-tree-design-vector.jpg" width="200px"> </p>

## Prediction
With the model trained, the prediction of the feature is made, and it is exported to a file for further evaluation.
