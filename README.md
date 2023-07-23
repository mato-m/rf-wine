# Random forest - Wine quality prediction
## Dataset
The downloaded [dataset](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009) contains
1599 rows and 12 columns. All columns have numeric values. The last column represents the quality prediction
of wine with given parameters such as acidity, level of sugar and level of alcohol. The goal is to create
a model that predicts the wine quality based on given parameters with high accuracy. There are no missing values.

## Model
The Quality column values range between 3 and 8. We can reduce the number of classes to two, which will be
easier to predict. We can say that wines that have quality below 6 have low quality, and good quality
if the quality is equal to six or more. The columns that have the highest correlation with wine Quality
are: Alcohol, Volatile Acidity, Total Sulfur Dioxide and Sulphates, so we will use these columns
as our input data.

The dataset is divided into training and test datasets, which contain 80% and 20% of data instances respectively.
The input values are scaled to values between 0 and 1.

## Random Forest algorithm
The model uses Random Forest algorithm. The Random Forest algorithm takes the average of multiple Decision trees
that were trained on different subsets of training set. The Random Forest algorithm uses bagging method
to improve the accuracy of a model by combining the predictions of different models.

Furthermore, we can also use bagging method to get the best results of multiple Random Forest models.
In this case, we use the aggregate of 10 Random Forest models, and each of those models use 100
decision trees in order to achieve the highest performance.

## Results
The model has achieved 81.25% accuracy score, 83.33% recall score and 81.25% F1 score.
