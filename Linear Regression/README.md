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
<th colspan="3"><img src=".\Images\heatmap.png" alt="" border='3' height='270' width='270' /></th>

---

* First point* : It's important our class attribute (MEDV) follow **Normal Distribution** or nearby this distribution.
<th colspan="3"><img src=".\Images\y dist.png" alt="" border='3' height='250' width='350' /></th>

---

### using **pairplot** to show the combination of scatter plot between diffrent features and histogram for each feature.
<th colspan="3"><img src=".\Images\paitplot.png" alt="" border='3' height='600' width='600' /></th>

#### I prefer to split the data to %85 train and %15 test set.

---

# Learning :
> First of all, we use LinearRegression module from sklearn.linear_model library.

#### Our model calculate the intercept value equal to :
**415635.4063567504**

#### also the other coefficient respectively for each feature is equal to : 
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

---

# Prediction:
<th colspan="3"><img src=".\Images\scatterplot_pred_real.png" alt="" border='3' height='250' width='350' /></th>

---

# Evaluation :
| metrics | Value |
|:---------|-----:|
| Mean Absolute Error (**MAE**) | 71424.14 |
| Mean Squared Error (**MSE**) | 9492233550.37 | 
| Root Mean Squared Error (**RMSE**) | 97428.09 |

---


*Second point*: The distribution plot shows the diffrence between real value and predicted value following a Normal distribution and this is a **good** result.
<th colspan="3"><img src=".\Images\dist_predict_real.png" alt="" border='3' height='290' width='400' /></th>

---

# Extra Work :
### I want to see that does Scaling on data affect on performance and pridiction evaluation in regression tasks?
* I Want First Scaling just on x_train and x_test and comparing with scaling on all data (include class attrubute or y).
##### I get these values after scalling on x_train and x_test which same as main model results :

| metrics | Value |
|:---------|-----:|
| Mean Absolute Error (**MAE**) | 71424.14 |
| Mean Squared Error (**MSE**) | 9492233550.37 | 
| Root Mean Squared Error (**RMSE**) | 97428.09 |

---

##### Also get below values after scalling on all data and then split data to train and test sets :
| metrics | Value |
|:---------|-----:|
| Mean Absolute Error (**MAE**) | 0.43 |
| Mean Squared Error (**MSE**) | 0.35 | 
| Root Mean Squared Error (**RMSE**) | 0.59 |

---

# Conclution:
* It can be concluded from this results that the results when we don't use scaling with just scaling on x_train and x_test is equl and scaling is useless.

* But the results when scaling implement on all data even class attribute we get some diffrent values for our metrics that use for evaluation.

* But i think this values can be valid and usefull for comparing and interpretation because the scatter plot which draw between true value and predicted value same as other models(no scaling and scaling on x).

* All in all, i think we have another view of our prediction and can be use as a tool for more exploration and making accurate decision.
<th colspan="3"><img src=".\Images\comparing.png" alt="" border='3' height='600' width='600' /></th>

