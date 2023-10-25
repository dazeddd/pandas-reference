
[Function application, GroupBy & window](https://pandas.pydata.org/docs/reference/frame.html#function-application-groupby-window)

```python
# how-to-apply-a-function-to-two-columns-of-pandas-dataframe
# https://stackoverflow.com/questions/13331698/how-to-apply-a-function-to-two-columns-of-pandas-dataframe
import pandas as pd

df = pd.DataFrame({'ID':['1', '2', '3'], 'col_1': [0, 2, 3], 'col_2':[1, 4, 5]})
mylist = ['a', 'b', 'c', 'd', 'e', 'f']

def get_sublist(sta,end):
    return mylist[sta:end+1]

df['col_3'] = df.apply(lambda x: get_sublist(x.col_1, x.col_2), axis=1)
# or
# df['col_3'] = df.apply(lambda x: get_sublist(x['col_1'], x['col_2']), axis=1)
```

[Missing data handling](https://pandas.pydata.org/docs/reference/frame.html#missing-data-handling)

```python
# drop empty row with column subset 
df.dropna(axis=0, how=all, subset=[])
```