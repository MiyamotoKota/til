bar_list = ax.bar(x,y, color='lightgray')
bar_list[4].set_color('blue')
ax.set_title('自治体別法人数における富士市の位置付け', fontsize=20);
ax.set_ylabel('法人数', fontsize=15)
ax.text(7.5, 9000, '上位１０の自治体を抜粋して表示', fontsize=15)

```python
tmp.sort_values(inplace=True, ascending=False)
tmp = tmp[:10]
x=tmp.index
y=tmp.values
fig, ax = plt.subplots(figsize=(20,10))
bar_list = ax.bar(x,y, color='lightgray')
bar_list[4].set_color('blue')
ax.set_title('自治体別法人数における富士市の位置付け', fontsize=20);
ax.set_ylabel('法人数', fontsize=15)
ax.text(7.5, 9000, '上位１０の自治体を抜粋して表示', fontsize=15)


```
