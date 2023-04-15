# shapfs

A python package makes feature selection by calculating the Shapley value

[The example of shapfs](https://github.com/JianyangHu/shapfs/blob/main/example/main.ipynb):
# Qucik usage guide

## Installation
You can install shapfs with [pip](https://pypi.org/project/shapfs/):
```
pip install shapfs
```


## Build the class of fs (features selection)

```
fs=feature_selection(type)
```

type=1 if the machine learning task is classification prediction. type=0 if it is regression prediction


## Fit fs
```
fs.fit(x,y,alpha)
```
x is the input feature, y is the label, and alpha is the ratio of the shaply value of the selected variable to the sum of all feature shapley values


## Result

After you fit the fs, you can view the Shapely values of all variables through fs.feature_ranking. fs.result gets the desired variable

```
fs.feature_ranking

fs.result
```

## Plot
You can also visualize the order of importance of features.

```
fs.feature_importance_plot()

fs.feature_beeswarm()
```

