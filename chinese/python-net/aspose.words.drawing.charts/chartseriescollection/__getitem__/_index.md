---
title: ChartSeriesCollection indexer
linktitle: ChartSeriesCollection indexer
articleTitle: ChartSeriesCollection indexer
second_title: Aspose.Words for Python
description: "ChartSeriesCollection indexer. Returns a [ChartSeries](../../chartseries/) at the specified index."
type: docs
weight: 10
url: /zh/python-net/aspose.words.drawing.charts/chartseriescollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Returns a [ChartSeries](../../chartseries/) at the specified index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows how to add and remove series data in a chart.

```python
# 插入一个柱状图，默认包含三个演示数据系列。
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart_data = chart.series
assert chart_data.count == 3
# 打印图表中每个系列的名称。
for series in chart.series:
    print(series.name)
# 这些是图表中类别的名称。
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# 我们可以为现有类别添加带有新值的系列。
# 此图表现在将包含四组每组四列的柱形。
chart.series.add(series_name='Series 4', categories=categories, values=[4.4, 7, 3.5, 2.1])
assert chart_data.count == 4
assert chart_data[3].name == 'Series 4'
# 也可以通过索引删除图表系列，如下所示。
# 这将删除图表附带的三个演示系列中的一个。
chart_data.remove_at(2)
assert not any([s.name == 'Series 3' for s in chart_data])
assert chart_data.count == 3
assert chart_data[2].name == 'Series 4'
# 我们也可以使用此方法一次性清除图表的所有数据。
# 创建新图表时，这是清除所有演示数据的方法
# 在我们开始处理空白图表之前。
chart_data.clear()
assert chart_data.count == 0
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

