# Neural Networks

Module 14 Challenge

[![Screen-Shot-2022-04-10-at-1-35-45-PM.png](https://i.postimg.cc/vTSJyq5t/Screen-Shot-2022-04-10-at-1-35-45-PM.png)](https://postimg.cc/JHZ6cQ6s)

# Background

In this Challenge, I’ll assume the role of a financial advisor at one of the top five financial advisory firms in the world. The firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, the firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave my firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. Thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, I’ll enhance the existing trading signals with machine learning algorithms that can adapt to new data.

---

## Technologies

The data we're analyzing comes from a jupyter notebook that we'll create and import files to. We'll be using Python to run and read our data. 

* [jupyter] - (https://github.com/jupyter/notebook) - Helps us run our code and get the information we need from the data listed in csv files.

---

## Installation Guide

In order for us to get the data we need we must import pandas, plots and the csv files we want to observe.

```python
# Imports
import pandas as pd
import numpy as np
from pathlib import Path
import hvplot.pandas
import matplotlib.pyplot as plt
from sklearn import svm
from sklearn.preprocessing import StandardScaler
from pandas.tseries.offsets import DateOffset
from sklearn.metrics import classification_report
from sklearn.linear_model import LogisticRegression
```


---
## Usage
* Attempting to improve on first model’s predictive accuracy.


```python
# Plot the actual returns versus the strategy returns for first predictions


(1 + predictions_df[["Actual Returns", "Strategy Returns"]]).cumprod().plot()
```
[![challenge-output.png](https://i.postimg.cc/X7RPgyLq/challenge-output.png)](https://postimg.cc/BXCNSbdf)

---
```python
# Plot the actual returns versus the strategy returns for second predictions

(1 + predictions_df2[["Actual Returns", "Strategy Returns"]]).cumprod().plot()
```
[![challenge-output-2.png](https://i.postimg.cc/c1jks8Vh/challenge-output-2.png)](https://postimg.cc/s1Y4m1fG)

---
## Evaluation Report
* Based on my findings the initial predictions for trade signals were more accurate in the first than the second round of predicitions that were made. You see a closer correlation to the actual returns and the strategy returns in the first predicted model.
  
* If you look at the second model it is far more innaccurate in prediciting the actual returns. The biggest innaccuracy is between 2020 and 2021.
  
* Our newly predicted model was less accurate thus I would recommend we use the initial predictions as the baseline for more improvement in the future.

Predicition 1  
  [![challenge-output.png](https://i.postimg.cc/X7RPgyLq/challenge-output.png)](https://postimg.cc/BXCNSbdf)

Predicition 2 
[![challenge-output-2.png](https://i.postimg.cc/c1jks8Vh/challenge-output-2.png)](https://postimg.cc/s1Y4m1fG)

---

## Contributors

Brought to you by Elgin Braggs Jr.

---
## License

MIT