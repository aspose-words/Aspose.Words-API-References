---
title: AxisScaling.maximum property
linktitle: maximum property
articleTitle: maximum property
second_title: Aspose.Words for Python
description: "AxisScaling.maximum property. Gets or sets the maximum value of the axis."
type: docs
weight: 30
url: /zh/python-net/aspose.words.drawing.charts/axisscaling/maximum/
---

## AxisScaling.maximum property

Gets or sets the maximum value of the axis.


```python
@property
def maximum(self) -> aspose.words.drawing.charts.AxisBound:
    ...

@maximum.setter
def maximum(self, value: aspose.words.drawing.charts.AxisBound):
    ...

```

### Remarks

The default value is "auto".


### Examples

Shows how to insert chart with date/time values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
# 清除图表的演示数据系列，以便从空白图表开始。
chart.series.clear()
# 添加一个自定义系列，X 轴包含日期/时间值，Y 轴包含相应的小数值。
chart.series.add_date(series_name='Aspose Test Series', dates=[datetime.datetime(2017, 11, 6), datetime.datetime(2017, 11, 9), datetime.datetime(2017, 11, 15), datetime.datetime(2017, 11, 21), datetime.datetime(2017, 11, 25), datetime.datetime(2017, 11, 29)], values=[1.2, 0.3, 2.1, 2.9, 4.2, 5.3])
# 设置 X 轴的下限和上限。
x_axis = chart.axis_x
# 将日期时间转换为 OLE 自动化日期（自 1899-12-30 起的天数）

def to_ole_autodate(dt):
    # 从 0001-01-01 到 1899-12-30 的天数是 693594
    delta = dt - datetime.datetime(1899, 12, 30)
    return delta.days + (dt.hour * 3600 + dt.minute * 60 + dt.second) / 86400.0
x_axis.scaling.minimum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 11, 5)))
x_axis.scaling.maximum = aw.drawing.charts.AxisBound(to_ole_autodate(datetime.datetime(2017, 12, 3)))
# 将 X 轴的主单位设置为一周，次单位设置为一天。
x_axis.base_time_unit = aw.drawing.charts.AxisTimeUnit.DAYS
x_axis.major_unit = 7
x_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
x_axis.minor_unit = 1
x_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.OUTSIDE
x_axis.has_major_gridlines = True
x_axis.has_minor_gridlines = True
# 为小数值定义 Y 轴属性。
y_axis = chart.axis_y
y_axis.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.HIGH
y_axis.major_unit = 100
y_axis.minor_unit = 50
y_axis.display_unit.unit = aw.drawing.charts.AxisBuiltInUnit.HUNDREDS
y_axis.scaling.minimum = aw.drawing.charts.AxisBound(100)
y_axis.scaling.maximum = aw.drawing.charts.AxisBound(700)
y_axis.has_major_gridlines = True
y_axis.has_minor_gridlines = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DateTimeValues.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisScaling](../)

