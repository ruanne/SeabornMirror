# How to plot error bands 

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

store = pd.read_csv('datasets/icecream_store_visitors.csv')
store.head()

mean = store['no_visitors'].mean()
stdev = store['no_visitors'].std()

ax = sns.lineplot(data=store, x='day', y='no_visitors')
ax.fill_between(store['day'], store['no_visitors'] - stdev, store['no_visitors'] + stdev, alpha=0.2)
```
