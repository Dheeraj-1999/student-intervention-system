Supervised Learning
# Student Intervention System


## quickly Check the code:
[code](https://web-resume-dng.herokuapp.com/assets/student_intervention1.html)
### Install

This project requires **Python 3+** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [scikit-learn](http://scikit-learn.org/stable/)



### Code

Template code is provided in the notebook `student_intervention.ipynb` notebook file. 

### Run

In a terminal or command window, navigate to the top-level project directory `student_intervention/` (that contains this README) and run one of the following commands:

```ipython notebook student_intervention.ipynb```  
```jupyter notebook student_intervention.ipynb```


### STEPS DONE:
- Explore the Data
- Preparing the Data
  - Identify feature and target columns
- Preprocess Feature Columns
- Implementation
  - Training and Testing Data Split
  - Model Application
  - Model Performance Metrics

#### explore the data:

- The total number of students, n_students.395
- The total number of features for each student, n_features. 30
- The number of those students who passed, n_passed. 265
- The number of those students who failed, n_failed. 130
- The graduation rate of the class, grad_rate, in percent (%).67.09

## Data

The dataset used in this project is included as `student-data.csv`. This dataset has the following attributes:

- `school` : student's school (binary: "GP" or "MS")
- `sex` : student's sex (binary: "F" - female or "M" - male)
- `age` : student's age (numeric: from 15 to 22)
- `address` : student's home address type (binary: "U" - urban or "R" - rural)
- `famsize` : family size (binary: "LE3" - less or equal to 3 or "GT3" - greater than 3)
- `Pstatus` : parent's cohabitation status (binary: "T" - living together or "A" - apart)
- `Medu` : mother's education (numeric: 0 - none,  1 - primary education (4th grade), 2 - 5th to 9th grade, 3 - secondary education or 4 - higher education)
- `Fedu` : father's education (numeric: 0 - none,  1 - primary education (4th grade), 2 - 5th to 9th grade, 3 - secondary education or 4 - higher education)
- `Mjob` : mother's job (nominal: "teacher", "health" care related, civil "services" (e.g. administrative or police), "at_home" or "other")
- `Fjob` : father's job (nominal: "teacher", "health" care related, civil "services" (e.g. administrative or police), "at_home" or "other")
- `reason` : reason to choose this school (nominal: close to "home", school "reputation", "course" preference or "other")
- `guardian` : student's guardian (nominal: "mother", "father" or "other")
- `traveltime` : home to school travel time (numeric: 1 - <15 min., 2 - 15 to 30 min., 3 - 30 min. to 1 hour, or 4 - >1 hour)
- `studytime` : weekly study time (numeric: 1 - <2 hours, 2 - 2 to 5 hours, 3 - 5 to 10 hours, or 4 - >10 hours)
- `failures` : number of past class failures (numeric: n if 1<=n<3, else 4)
- `schoolsup` : extra educational support (binary: yes or no)
- `famsup` : family educational support (binary: yes or no)
- `paid` : extra paid classes within the course subject (Math or Portuguese) (binary: yes or no)
- `activities` : extra-curricular activities (binary: yes or no)
- `nursery` : attended nursery school (binary: yes or no)
- `higher` : wants to take higher education (binary: yes or no)
- `internet` : Internet access at home (binary: yes or no)
- `romantic` : with a romantic relationship (binary: yes or no)
- `famrel` : quality of family relationships (numeric: from 1 - very bad to 5 - excellent)
- `freetime` : free time after school (numeric: from 1 - very low to 5 - very high)
- `goout` : going out with friends (numeric: from 1 - very low to 5 - very high)
- `Dalc` : workday alcohol consumption (numeric: from 1 - very low to 5 - very high)
- `Walc` : weekend alcohol consumption (numeric: from 1 - very low to 5 - very high)
- `health` : current health status (numeric: from 1 - very bad to 5 - very good)
- `absences` : number of school absences (numeric: from 0 to 93)
- `passed` : did the student pass the final exam (binary: yes or no)

#### Preparing the Data

In this section, prepare the data for modeling, training and testing.

#### Preprocess Feature Columns

There are several non-numeric columns that need to be converted! Many of them are simply yes/no. These can be reasonably converted into 1/0 (binary) values.

These generated columns are sometimes called dummy variables, and we will use the pandas.get_dummies() function to perform this transformation.

#### Training and Testing Data Split

- randomly shuffle and split the data (X_all, y_all) into training and testing subsets.
- Use 300 training points (approximately 75%) and 95 testing points (approximately 25%).

#### Training

- Ensemble Methods (XgBoost, Random Forest)
- K-Nearest Neighbors (KNeighbors)
- Support Vector Machines (SVM)
- Logistic Regression

#### Evaluating Models
- RANDOM FOREST CLASSIFIER:
  - F1 score for training set: 0.8189.
  - F1 score for test set: 0.8101.
  - acc score for training set: 0.7067.
  - acc score for test set: 0.6842.
- XGBOOST CLASSIFIER:
  - F1 score for training set: 0.7950.
  - F1 score for test set: 0.8101.
  - acc score for training set: 0.6700.
  - acc score for test set: 0.6842.
- LogisticRegression:
  - F1 score for training set: 0.8492.
  - F1 score for test set: 0.7273.
  - acc score for training set: 0.7833.
  - acc score for test set: 0.6211.

- Support vector machine:
  - F1 score for training set: 0.8230.
  - F1 score for test set: 0.8153.
  - acc score for training set: 0.7133.
  - acc score for test set: 0.6947.
  
 
KNeighborsClassifier:
  - F1 score for training set: 0.8515.
  - F1 score for test set: 0.7917.
  - acc score for training set: 0.7933.
  - acc score for test set: 0.6844.

## FUTURE WORK TO BE DONE:
WANT TO DEPLOY THIS MODEL AND GIVE THIS PROJECT A USER INTERFACE.
