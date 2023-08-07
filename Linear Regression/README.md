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
  <table>
  <tr>
    <td><span style="font-weight:bold">Python Overview [</span><a href="http://people.uncw.edu/chenc/STT592_Deep%20Learning/Python/Python%20Overview.docx"><span style="font-weight:bold">Word</span></a><span style="font-weight:bold">]</span><br><br><br><span style="font-weight:bold">Python Tutorial [</span><a href="http://people.uncw.edu/chenc/STT592_Deep%20Learning/Python/python_intro.pdf"><span style="font-weight:bold">PDF</span></a><span style="font-weight:bold">]  [</span><a href="http://people.uncw.edu/chenc/STT592_Deep%20Learning/Python/python_tutorial2.pdf"><span style="font-weight:bold">Code</span></a><span style="font-weight:bold">]</span></td>
    <td><span style="font-weight:bold">Numpy [</span><a href="http://people.uncw.edu/chenc/STT592_Deep%20Learning/Python/python_tutorial2.pdf"><span style="font-weight:bold">PDF</span></a><span style="font-weight:bold">] [</span><a href="http://people.uncw.edu/chenc/STT592_Deep%20Learning/Python/Kling_Python%20Scripts/numpy_tutorial.py"><span style="font-weight:bold">Code</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">User Guide [</span><a href="https://docs.scipy.org/doc/numpy-1.15.0/index.html"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Quickstart [</span><a href="https://docs.scipy.org/doc/numpy-1.15.0/user/quickstart.html"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Reference [</span><a href="https://docs.scipy.org/doc/numpy-1.15.0/reference/index.html"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Practice Numpy in LabEx [</span><a href="https://labex.io/courses/100-numpy-exercises"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Cheatsheet [</span><a href="http://www.utc.fr/~jlaforet/Suppl/python-cheatsheets.pdf"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span></td>
    <td><span style="font-weight:bold">Matplotlib [</span><a href="http://people.uncw.edu/chenc/STT592_Deep%20Learning/Python/python_tutorial2.pdf"><span style="font-weight:bold">PDF</span></a><span style="font-weight:bold">][</span><a href="http://people.uncw.edu/chenc/STT592_Deep%20Learning/Python/Kling_Python%20Scripts/matplotlib_tutorial.py"><span style="font-weight:bold">Code</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Example [</span><a href="https://matplotlib.org/gallery/index.html#"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Tutorials [</span><a href="https://matplotlib.org/tutorials/index.html"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Reference [</span><a href="https://matplotlib.org/api/_as_gen/matplotlib.pyplot.html"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Practice Matplotlib in LabEx [</span><a href="https://labex.io/courses/draw-2d-and-3d-graphics-by-matplotlib"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Cheatsheet [</span><a href="http://www.utc.fr/~jlaforet/Suppl/python-cheatsheets.pdf"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span></td>
  </tr>
  <tr>
    <td><span style="font-weight:bold">Pandas [</span><a href="http://people.uncw.edu/chenc/STT592_Deep%20Learning/Python/Pandas_tutorial.py"><span style="font-weight:bold">Code</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">10 Min to Pandas [</span><a href="https://pandas.pydata.org/pandas-docs/stable/10min.html"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Cookbook [</span><a href="https://pandas.pydata.org/pandas-docs/stable/cookbook.html"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Tutorials [</span><a href="https://pandas.pydata.org/pandas-docs/stable/tutorials.html"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Reference [</span><a href="https://pandas.pydata.org/pandas-docs/stable/"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Practice Pandas in LabEx [</span><a href="https://labex.io/courses/100-pandas-exercises"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Cheatsheet [</span><a href="http://www.utc.fr/~jlaforet/Suppl/python-cheatsheets.pdf"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span></td>
    <td><span style="font-weight:bold">Seaborn: Stat data </span><br><span style="font-weight:bold">Visulization [</span><a href="https://seaborn.pydata.org/"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Example [</span><a href="https://seaborn.pydata.org/examples/index.html"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Tutorials [</span><a href="https://seaborn.pydata.org/tutorial.html"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Reference [</span><a href="https://seaborn.pydata.org/api.html#api-ref"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Cheatsheet [</span><a href="http://www.utc.fr/~jlaforet/Suppl/python-cheatsheets.pdf"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span></td>
    <td><span style="font-weight:bold">Scikit Learn [</span><a href="https://scikit-learn.org/stable/?fbclid=IwAR0DE6Q4LLO48d226SwF8j6TbUoqjBw769bNEcOBF9ohBW8Wgz9WscvgzEw"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">] </span><br><span style="font-weight:bold">Scikit Image [</span><a href="http://scikit-image.org/docs/dev/auto_examples/?fbclid=IwAR3v-V5IlW1Jjz-NcSbGuDFJ71KUFRk5KmPoFRCD8LuuAyTzUF8v0N4nwUU"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Scikit Tutorial #1 [</span><a href="http://people.uncw.edu/chenc/STT592_Deep%20Learning/Python/Kling_Python%20Scripts/scikit_tutorial.py"><span style="font-weight:bold">Code</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Scikit Tutorial #2 [</span><a href="http://people.uncw.edu/chenc/STT592_Deep%20Learning/Python/Kling_Python%20Scripts/scikit_tutorial2.py"><span style="font-weight:bold">Code</span></a><span style="font-weight:bold">]</span><br><span style="font-weight:bold">Cheatsheet [</span><a href="https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Scikit_Learn_Cheat_Sheet_Python.pdf"><span style="font-weight:bold">Link</span></a><span style="font-weight:bold">]</span></td>
  </tr>
</table>
