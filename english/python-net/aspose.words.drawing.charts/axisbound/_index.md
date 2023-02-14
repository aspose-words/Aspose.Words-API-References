---
title: AxisBound class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents minimum or maximum bound of axis values"
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/axisbound/
---

## AxisBound class

Represents minimum or maximum bound of axis values.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




Bound can be specified as a numeric, datetime or a special "auto" value.

The instances of this class are immutable.




### Constructors
| Name | Description |
| --- | --- |
| [AxisBound()](./__init__/#default) | Creates a new instance indicating that axis bound should be determined automatically by a word-processing application. |
| [AxisBound(value)](./__init__/#float) | Creates an axis bound represented as a number. |
| [AxisBound(datetime)](./__init__/#datetime) | Creates an axis bound represented as datetime value. |

### Properties

| Name | Description |
| --- | --- |
| [is_auto](./is_auto/) | Returns a flag indicating that axis bound should be determined automatically. |
| [value](./value/) | Returns numeric value of axis bound. |
| [value_as_date](./value_as_date/) | Returns value of axis bound represented as datetime. |

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

### See Also

* module [aspose.words.drawing.charts](../)
* property [AxisScaling.minimum](../axisscaling/minimum/)
* property [AxisScaling.maximum](../axisscaling/maximum/)

