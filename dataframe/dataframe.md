
[Function application, GroupBy & window](https://pandas.pydata.org/docs/reference/frame.html#function-application-groupby-window)

[Missing data handling](https://pandas.pydata.org/docs/reference/frame.html#missing-data-handling)

```python
# drop empty row with column subset 
df.dropna(axis=0, how=all, subset=[])
```