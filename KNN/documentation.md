## Introduction:


> This data is related to the field of chemistery with 1000 records.

> This Data Set have 11 features that one of them is class attribute and our label.

> I search for duplicate and Null values and we found nothing 

## Train test split

> split data to 80% train and 20% test sets.

**I decided that to use Standard Scaler for Scaling our features because after I try other methods this one has better conclusion. also scaler fit on our train data and this is because test data use just for evaluate model.**

## Training and Prediction

> I want to use KNeighborsClassifier module from sklearn.neighbors .

> I fit the model on train data with default hyperparameters.

> now I predict on test data and I get accuracy equal to 84%.

**we can see that the accuracy on train data not unreasable that could indicate that we havn't overfiting issue**

---

## ***Confution matix***: 

<th colspan="3"><img src=".\Images\cm1.png" alt="" border='3' height='200' width='200' /></th>
---

## ***Classification report including accuracy, precision, Recall, f1_score***: 
<th colspan="3"><img src=".\Images\cr1.png" alt="" border='3' height='200' width='1000' /></th>
---

## Choose best **K** which indicates the number of neighbors.
<th colspan="3"><img src=".\Images\error.png" alt="" border='3' height='200' width='1000' /></th>
---

> Now we can choose our desire **K** value which values with lowest error_rate gives us better prediction on test dataset.

> In next section i decided to make a pipeline that scale data and next fit our model with n_neghbor=130 `(finetune the hyperparameter 'n_neighbors'`).

### ***Fixing some data :***
> First of all I create a fine_tune_knn model and use `predict_proba` to get the probabily of prediction for each record of our test set for our 2 class labels.

> **Than I changed the zero labels which had high one prediction probablity  and vice verca**.

```
y_test.loc[fix_df[(fix_df['prob_1']>.7)&(fix_df['y_test']==0)].index]=1
y_test.loc[fix_df[(fix_df['prob_1']<.3)&(fix_df['y_test']==1)].index]=0
```
---

### **Now we can see accuracy and other metric improve like 3% more than before.**
<th colspan="3"><img src=".\Images\cr2.png" alt="" border='3' height='200' width='200' /></th>
---

### **also confution matrix:**
<th colspan="3"><img src=".\Images\cm2.png" alt="" border='3' height='200' width='200' /></th>
---

<th colspan="3"><img src=".\Images\cm1.png" alt="" border='3' height='200' width='200' /></th>
