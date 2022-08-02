---
title: is_auto property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns a flag indicating that axis bound should be determined automatically."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.charts/axisbound/is_auto/
---

## AxisBound.is_auto property

Returns a flag indicating that axis bound should be determined automatically.


### Examples

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

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisBound](../)

