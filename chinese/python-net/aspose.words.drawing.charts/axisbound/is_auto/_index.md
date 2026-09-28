---
title: AxisBound.is_auto property
linktitle: is_auto property
articleTitle: is_auto property
second_title: Aspose.Words for Python
description: "AxisBound.is_auto property. Returns a flag indicating that axis bound should be determined automatically."
type: docs
weight: 20
url: /zh/python-net/aspose.words.drawing.charts/axisbound/is_auto/
---

## AxisBound.is_auto property

Returns a flag indicating that axis bound should be determined automatically.


```python
@property
def is_auto(self) -> bool:
    ...

```

### Examples

Shows how to set custom axis bounds.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SCATTER, width=450, height=300)
chart = chart_shape.chart
# 清除图表的演示数据系列，以便从空白图表开始。
chart.series.clear()
# 添加一个包含两个十进制数组的系列。第一个数组包含 X 值，
# 第二个数组包含散点图中点的对应 Y 值。
chart.series.add_double(series_name='Series 1', x_values=[1.1, 5.4, 7.9, 3.5, 2.1, 9.7], y_values=[2.1, 0.3, 0.6, 3.3, 1.4, 1.9])
# 默认情况下，图表的 X 轴和 Y 轴会应用默认缩放，
# 以确保它们的范围足够大，能够容纳每个系列的所有 X 值和 Y 值。
self.assertTrue(chart.axis_x.scaling.minimum.is_auto)
# 我们可以定义自己的轴范围。
# 在这种情况下，我们将使 X 轴和 Y 轴的刻度显示 0 到 10 的范围。
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
chart.axis_y.scaling.minimum = aw.drawing.charts.AxisBound(value=0)
chart.axis_y.scaling.maximum = aw.drawing.charts.AxisBound(value=10)
self.assertFalse(chart.axis_x.scaling.minimum.is_auto)
self.assertFalse(chart.axis_y.scaling.minimum.is_auto)
# 创建一个折线图，其中系列在 X 轴上需要日期范围，Y 轴上使用十进制值。
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=300)
chart = chart_shape.chart
chart.series.clear()
dates = [datetime.datetime(1973, 5, 11), datetime.datetime(1981, 2, 4), datetime.datetime(1985, 9, 23), datetime.datetime(1989, 6, 28), datetime.datetime(1994, 12, 15)]
chart.series.add_date(series_name='Series 1', dates=dates, values=[3, 4.7, 5.9, 7.1, 8.9])
# 我们也可以以日期形式设置轴范围，以限制图表的时间段。
# 将范围设置为 1980-1990 将省略系列中两个超出范围的值
# 这些值位于图表范围之外。
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1980, 1, 1))
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(datetime=datetime.datetime(1990, 1, 1))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisBound.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisBound](../)

