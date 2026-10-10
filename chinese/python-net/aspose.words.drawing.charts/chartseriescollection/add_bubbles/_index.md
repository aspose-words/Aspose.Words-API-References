---
title: ChartSeriesCollection.add_bubbles method
linktitle: add_bubbles method
articleTitle: add_bubbles method
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.add_bubbles method. Adds new [ChartSeries](../../chartseries/) to this collection"
type: docs
weight: 40
url: /zh/python-net/aspose.words.drawing.charts/chartseriescollection/add_bubbles/
---

## add_bubbles(series_name, x_values, y_values, bubble_sizes) {#str_floatlist_floatlist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Bubble charts.



```python
def add_bubbles(self, series_name: str, x_values: List[float], y_values: List[float], bubble_sizes: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| x_values | List[float] |  |
| y_values | List[float] |  |
| bubble_sizes | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


### Examples

Shows how to create an appropriate type of chart series for a graph type.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 填充图表系列集合有多种方法。
# 不同的系列模式适用于不同的图表类型。
# 1 - 按类别在 X 轴上分组和分带的柱状图：
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.COLUMN, 500, 300)
categories = ['Category 1', 'Category 2', 'Category 3']
# 插入两个包含每个相应类别值的小数值系列。
# 此柱状图将有三个组，每组包含两根柱子。
chart.series.add(series_name='Series 1', categories=categories, values=[76.6, 82.1, 91.6])
chart.series.add(series_name='Series 2', categories=categories, values=[64.2, 79.5, 94])
# 类别沿 X 轴分布，数值沿 Y 轴分布。
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 2 - 日期沿 X 轴分布的面积图：
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.AREA, 500, 300)
dates = [datetime.datetime(2014, 3, 31), datetime.datetime(2017, 1, 23), datetime.datetime(2017, 6, 18), datetime.datetime(2019, 11, 22), datetime.datetime(2020, 9, 7)]
# 插入一个系列，为每个相应的日期提供小数值。
# 这些日期将沿线性 X 轴分布，
# 并且添加到此系列的数值将形成数据点。
chart.series.add_date(series_name='Series 1', dates=dates, values=[15.8, 21.5, 22.9, 28.7, 33.1])
self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 3 - 2D 散点图：
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.SCATTER, 500, 300)
# 每个系列需要两个等长的十进制数组。
# 第一个数组包含 X 值，第二个数组包含相应的 Y 值
# 图表图形上的数据点。
chart.series.add_double(series_name='Series 1', x_values=[3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6], y_values=[3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9])
chart.series.add_double(series_name='Series 2', x_values=[2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3], y_values=[7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6])
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_x.type)
self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
# 4 - 气泡图：
chart = ExCharts._append_chart(builder, aw.drawing.charts.ChartType.BUBBLE, 500, 300)
# 每个系列需要三个等长的十进制数组。
# 第一个数组包含 X 值，第二个数组包含相应的 Y 值，
# 第三个数组包含图形中每个数据点的直径。
chart.series.add_bubbles(series_name='Series 1', x_values=[1.1, 5, 9.8], y_values=[1.2, 4.9, 9.9], bubble_sizes=[2, 4, 8])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartSeriesCollection.docx')
```

Shows how to create an appropriate type of chart series for a graph type (AppendChart).

```python
@staticmethod
def _append_chart(builder, chart_type, width, height):
    chart_shape = builder.insert_chart(chart_type=chart_type, width=width, height=height)
    chart = chart_shape.chart
    chart.series.clear()
    return chart
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

