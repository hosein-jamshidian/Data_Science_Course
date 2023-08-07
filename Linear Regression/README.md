# Data Introduction:
> I decided to use a machine learning algorithm that named Linear regression for regression task on prediction house price.

> This data set has 489 records (rows) and 4 features (columns).
> 
[**access data**](https://github.com/hosein-jamshidian/Data_Science_Course/blob/main/Linear%20Regression/Data/boston_housing.csv)


## description of our features:
1. **RM** : average number of rooms per dwelling.
2. **LSTAT** : lower status of the population.
3. **PTRATION** : pupil-teacher ratio by town.
4. **MEDV** : Median value of owner-occupied homes in $1000's.

## show correlation between features using heatmap:
<th colspan="3"><img src=".\Images\heatmap.png" alt="" border='3' height='300' width='300' /></th>

---

*point* : It's important our class attribute (MEDV) follow **Normal Distribution** or nearby this distribution.
<th colspan="3"><img src=".\Images\y dist.png" alt="" border='3' height='250' width='350' /></th>

---

### using **pairplot** to show the combination of scatter plot between diffrent features and histogram for each feature.
<th colspan="3"><img src=".\Images\paitplot.png" alt="" border='3' height='600' width='600' /></th>

> I prefer to split the data to %85 train and %15 test set.

---

# Learning and Prediction:
> First of all, we use LinearRegression module from sklearn.linear_model library.

#### Our model calculate the intercept value equal to : **415635.4063567504** and also the other coefficient respectively for each feature is equal to : 
[ 83746.05285138,  -11026.20851495,  -18580.49871423]

## Coefficient Interpretation:
| Features | Coef |
|:---------|-----:|
| **RM** | 83746.052851 |
| **LSTAT** | -11026.208515 | 
| **PTRATION** | -18580.498714 |

* Holding all other features fixed, a 1 unit increase in average number of rooms is associated with an **increase of $83746.05**.
* Holding all other features fixed, a 1 unit increase in population status is associated with an **decrease of $-11026.20**.
* Holding all other features fixed, a 1 unit increase in pupil_teacher ratio is associated with an **decrease of $-18580.49**.
