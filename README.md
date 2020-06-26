# machine-learning-challenge
The repo houses 3 machine learning models to predict if a newly discovered celestial body will be classified as an Exoplanet.
## [Data](data/clean_data.csv)
Data was obtained from [Kaggle](https://www.kaggle.com/nasa/kepler-exoplanet-search-results) and refined with a [cleaning program](data/cleaning.ipynb).
## Summary of Models
All models were tested against 25 different random samples of 40% of the data. Models are listed in order of their Accuracy from greatest to least.
Models were trained using 60% of the data.
### 1. [Deep Neural Network](models/DNN.ipynb)
This model is a Neural Network consisting of:
* 20 Input nodes
* 3 Background Layers
  * 100 nodes each
* 3 Output nodes
Model was trained with 100 epochs.
Test data tended to be around .94-.95 with a loss of .23-.27 
### 2. [Random Forest Model](models/random_forest.ipynb)
This model is a Random Forest Model using 20 input variables to determine the classification of the body.
It was created using 1000 estimators.
Accuracy was between .89-.91 for the testing data.
### 3. [K Nearest Neigbors Model](models/KNN.ipynb)
This model is a K Nearest Neigbors model using 20 input variables to determine the classification of the body.
It checks the data against the 39 nearest neigbors.
Accuracy was between .79-.81 for the testing data.
## Conclusion
The Deep Neural Network provided the best accuracy for testing data predictions. As such it's [model](model/DNN.h5) was
saved for purposes of use in making live predictions. More data and processing power could be used to create a network with
more input nodes and background layers/nodes to decrease loss in the model. More epochs could also be used with stronger processing
power, but would have to be careful to not overtrain the model.
## Built With
* Pandas
* Sci-kit Learn
* [NASA Kepler Data](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)
## Authors
* Ryan Klueg
