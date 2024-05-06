---
title: AxisTimeUnit enumeration
linktitle: AxisTimeUnit enumeration
articleTitle: AxisTimeUnit enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisTimeUnit enumeration. Specifies the unit of time for axes."
type: docs
weight: 120
url: /python-net/aspose.words.drawing.charts/axistimeunit/
---

## AxisTimeUnit enumeration

Specifies the unit of time for axes.


### Members

| Name | Description |
| --- | --- |
| AUTOMATIC | Specifies that unit was not set explicitly and default value should be used. |
| DAYS | Specifies that the chart data shall be shown in days. |
| MONTHS | Specifies that the chart data shall be shown in months. |
| YEARS | Specifies that the chart data shall be shown in years. |

### Examples

Shows how to insert chart with date/time values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.LINE, 500, 300)
chart = shape.chart

# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()

# Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
dates = [
    date(2017, 11, 6),
    date(2017, 11, 9),
    date(2017, 11, 15),
    date(2017, 11, 21),
    date(2017, 11, 25),
    date(2017, 11, 29)
    ]
chart.series.add("Aspose Test Series", dates=dates, values=[1.2, 0.3, 2.1, 2.9, 4.2, 5.3])

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
x_axis.has_major_gridlines = True
x_axis.has_minor_gridlines = True

# Define Y-axis properties for decimal values.
y_axis = chart.axis_y
y_axis.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.HIGH
y_axis.major_unit = 100.0
y_axis.minor_unit = 50.0
y_axis.display_unit.unit = aw.drawing.charts.AxisBuiltInUnit.HUNDREDS
y_axis.scaling.minimum = aw.drawing.charts.AxisBound(100)
y_axis.scaling.maximum = aw.drawing.charts.AxisBound(700)
y_axis.has_major_gridlines = True
y_axis.has_minor_gridlines = True

doc.save(ARTIFACTS_DIR + "Charts.date_time_values.docx")
```

### See Also

* module [aspose.words.drawing.charts](../)

