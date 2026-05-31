Assignment 1: Evaluate Regression and Classifier Metrics

Background
Learning to evaluate model performance based on metrics is a fundamental skill in predictive analytics.  You will use that skill this week.

Instructions
For this assignment,

You will load the iris dataset in Python.

from sklearn import datasets

iris= pd.DataFrame(datasets.load_iris().data)

iris.columns = datasets.load_iris().feature_names

iris['type'] = datasets.load_iris().target

iris['type']=iris['type'].astype('object')

iris
Create a new feature by multiplying sepal length by sepal width and dividing by petal length * petal width.
iris['new']=(iris.iloc[:,0]*iris.iloc[:,1])/(iris.iloc[:,2]*iris.iloc[:,3])
Sample 80% of the data for a training set stratifying on ‘type’
from sklearn.model_selection import train_test_split as tts
X_train, X_test, y_train, y_test = tts(iris.iloc[:,0:3], iris.iloc[:,4], test_size=0.2, random_state=42,
stratify=iris.iloc[:,4])
On the test set, evaluate the following two estimators for sepal width using ME, MPE, MAPE, MAE, and  MSE.

Mean of petal length calculated only on the training data

Mean of sepal length minus petal width calculated only on the training data

est1=np.mean(X_train['petal length (cm)'])

est2=np.mean(X_train['sepal length (cm)']-X_train['petal width (cm)'])

est1=[est1]*len(y_test)

est2=[est2]*len(y_test)

myf(X_test['sepal width (cm)'],est1)

myf(X_test['sepal width (cm)'],est2)
On the test set, evaluate the two classifiers (built on the training set) below for ‘type’ using accuracy, precision, recall, and the F1 score.
Up to 1st quantile of sepal length = type 0, >1st up to 2d quantile = type 1, >2d quantile = type 2

Up to 2d quantile of sepal length = type 0, >2d up to 3d quantile = type 1, >3d quantile = type 2

from numpy import percentile

est3=percentile(X_train['sepal length (cm)'], [25, 50])

y_hat=np.zeros(len(y_test))

y_hat[X_test['sepal length (cm)']>est3[0]]=1

y_hat[X_test['sepal length (cm)']>est3[1]]=2

y_hat=y_hat.astype('int')

print(cr(y_test.astype('int'),y_hat))

est4=percentile(X_train['sepal length (cm)'], [50,75])

y_hat2=np.zeros(len(y_test))

y_hat2[X_test['sepal length (cm)']>est3[0]]=1

y_hat2[X_test['sepal length (cm)']>est3[1]]=2

y_hat2=y_hat2.astype('int')

print(cr(y_test.astype('int'),y_hat2))
Interpret all of your findings.  Which model performed better as the regressor?  As the classifier?  What would you do to improve these models?
Length
This assignment must be 1 page plus the Python Notebook (must be shared).

Reference
Include 3 scholarly resources that address 1) previous and recent work on the topic, 2) theoretical considerations, and 3)  applications.
