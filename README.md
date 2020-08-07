
# Student Intervention System

## goal:
utilize  machine  learning  techniques  to  break down  and  discover  student  academic  performance  and  to enhance   the   nature   of   the   education   framework.The administrations  can  utilize  these  systems  to  enhance  the course  results  to  enhance  the  student  performance.  Such information can be utilized to give a decent comprehension of   student’s   enrollment pattern  in  the  courses  under study.

In Future  this  kind  of  analysis  can  be  implemented  with  a bigger  dataset  and  more  background  factors  of  student  at the  first-year  academic  level.

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

QUES: WHY MAKING DUMMY VARIABLES?
ANS: what if we wanted to also know if favorite class (e.g., science, math, and language) corresponded with an increased GPA. Let’s say we coded this so that science = 1, math = 2, and language = 3. Looking at the nominal favorite class variable, we can see that there is no such thing as an increase in favorite class – math is not higher than science, and is not lower than language either. This is sometimes referred to as directionality, and knowing that a high versus low score means something is an integral part of regression analysis. 

Dummy coding allows us to turn categories into something a regression can treat as having a high (1) and low (0) score. Any binary variable can be thought of as having directionality, because if it is higher, it is category 1, but if it is lower, it is category 0. This allows the regression look at directionality by comparing two sides, rather than expecting each unit to correspond with some kind of increase.

#### Training and Testing Data Split

- randomly shuffle and split the data (X_all, y_all) into training and testing subsets.
- Use 300 training points (approximately 75%) and 95 testing points (approximately 25%).

#### Training

- Ensemble Methods (XgBoost, Random Forest)
- K-Nearest Neighbors (KNeighbors)
- Support Vector Machines (SVM)
- Logistic Regression



#### Evaluating Models and MODELS PROPERTIES:
### - RANDOM FOREST CLASSIFIER (Ensemble based):
  - F1 score for training set: 0.8189.
  - F1 score for test set: 0.8101.
  - acc score for training set: 0.7067.
  - acc score for test set: 0.6842.
  
Strengths	
- Handles binary features well because it is an ensemble of decision trees.
- Handle high dimensional spaces and large numbers of training examples well.
- Does not expect linear features or features that interact linearly.
  
### - XGBOOST CLASSIFIER:
  - F1 score for training set: 0.7950.
  - F1 score for test set: 0.8101.
  - acc score for training set: 0.6700.
  - acc score for test set: 0.6842.
  
### - LogisticRegression:
  - F1 score for training set: 0.8492.
  - F1 score for test set: 0.7273.
  - acc score for training set: 0.7833.
  - acc score for test set: 0.6211.

Strengths	
- Is simple and has low variance -> robust to noise and is less likely to over-fit.

### - Support vector machine (Instance Based):
  - F1 score for training set: 0.8230.
  - F1 score for test set: 0.8153.
  - acc score for training set: 0.7133.
  - acc score for test set: 0.6947.

Strenghts:
- It works really well with a clear margin of separation
- It is effective in high dimensional spaces.
- It is effective in cases where the number of dimensions is greater than the number of samples.
- It uses a subset of training points in the decision function (called support vectors), so it is also memory efficient.

Limitations:
- It doesn’t perform well when we have large data set because the required training time is higher
- It also doesn’t perform very well, when the data set has more noise i.e. target classes are overlapping
 
# - KNeighborsClassifier (Instance Based):
  - F1 score for training set: 0.8515.
  - F1 score for test set: 0.7917.
  - acc score for training set: 0.7933.
  - acc score for test set: 0.6844.

Reference documents:
[What are the advantages of different classification algorithms?](https://www.quora.com/What-are-the-advantages-of-different-classification-algorithms)


### ANALYSIS:

- F1 score measure is taken to find student’s performance. F1 score achieves its best value at 1 and worst at 0.For finding the best model among the selected models first sample data of  100  students  was  tested  and  F1  score  is  calculated,  then sample size 200 students were taken and finally same model is  tested  with  sample  size  of  300  records.

## FUTURE WORK TO BE DONE:
WANT TO DEPLOY THIS MODEL AND GIVE THIS PROJECT A USER INTERFACE.
