---
title: AxisBound constructor
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.drawing.charts.AxisBound constructor"
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/axisbound/__init__/
---

## AxisBound() {#default}

Creates a new instance indicating that axis bound should be determined automatically by a word-processing
application.


```python
def __init__(self):
    ...
```

## AxisBound(value) {#float}

Creates an axis bound represented as a number.


```python
def __init__(self, value: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | float |  |

## AxisBound(datetime) {#datetime}

Creates an axis bound represented as datetime value.


```python
def __init__(self, datetime: datetime):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| datetime | datetime |  |

## Examples

Shows how to insert chart with date/time values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.LINE, 500, 300)
chart = shape.chart

# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()

# Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
chart.series.add("Aspose Test Series",
    [
        date(2017, 11, 6), date(2017, 11, 9), date(2017, 11, 15),
        date(2017, 11, 21), date(2017, 11, 25), date(2017, 11, 29)
    ],
    [1.2, 0.3, 2.1, 2.9, 4.2, 5.3])

# Set lower and upper bounds for the X-axis.
x_axis = chart.axis_x
x_axis.scaling.minimum = aw.drawing.charts.AxisBound(date(2017, 11, 5))
x_axis.scaling.maximum = aw.drawing.charts.AxisBound(date(2017, 12, 3))

# Set the major units of the X-axis to a week, and the minor units to a day.
x_axis.base_time_unit = aw.drawing.charts.AxisTimeUnit.DAYS
x_axis.major_unit = 7.0
x_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
x_axis.minor_unit = 1.0
x_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.OUTSIDE

# Define Y-axis properties for decimal values.
y_axis = chart.axis_y
y_axis.tick_label_position = aw.drawing.charts.AxisTickLabelPosition.HIGH
y_axis.major_unit = 100.0
y_axis.minor_unit = 50.0
y_axis.display_unit.unit = aw.drawing.charts.AxisBuiltInUnit.HUNDREDS
y_axis.scaling.minimum = aw.drawing.charts.AxisBound(100)
y_axis.scaling.maximum = aw.drawing.charts.AxisBound(700)

doc.save(ARTIFACTS_DIR + "Charts.date_time_values.docx")
```

Shows how to set custom axis bounds.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

chart_shape = builder.insert_chart(aw.drawing.charts.ChartType.SCATTER, 450, 300)
chart = chart_shape.chart

# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()

# Add a series with two decimal arrays. The first array contains the X-values,
# and the second contains corresponding Y-values for points in the scatter chart.
chart.series.add("Series 1",
    [1.1, 5.4, 7.9, 3.5, 2.1, 9.7],
    [2.1, 0.3, 0.6, 3.3, 1.4, 1.9])

# By default, default scaling is applied to the graph's X and Y-axes,
# so that both their ranges are big enough to encompass every X and Y-value of every series.
self.assertTrue(chart.axis_x.scaling.minimum.is_auto)

# We can define our own axis bounds.
# In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(0)
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(10)
chart.axis_y.scaling.minimum = aw.drawing.charts.AxisBound(0)
chart.axis_y.scaling.maximum = aw.drawing.charts.AxisBound(10)

self.assertFalse(chart.axis_x.scaling.minimum.is_auto)
self.assertFalse(chart.axis_y.scaling.minimum.is_auto)

# Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
chart_shape = builder.insert_chart(aw.drawing.charts.ChartType.LINE, 450, 300)
chart = chart_shape.chart
chart.series.clear()

dates = [
    date(1973, 5, 11),
    date(1981, 2, 4),
    date(1985, 9, 23),
    date(1989, 6, 28),
    date(1994, 12, 15)
    ]

chart.series.add("Series 1", dates, [3.0, 4.7, 5.9, 7.1, 8.9])

# We can set axis bounds in the form of dates as well, limiting the chart to a period.
# Setting the range to 1980-1990 will omit the two of the series values
# that are outside of the range from the graph.
chart.axis_x.scaling.minimum = aw.drawing.charts.AxisBound(date(1980, 1, 1))
chart.axis_x.scaling.maximum = aw.drawing.charts.AxisBound(date(1990, 1, 1))

doc.save(ARTIFACTS_DIR + "Charts.axis_bound.docx")
```

## See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisBound](../)

