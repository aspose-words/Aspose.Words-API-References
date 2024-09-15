---
title: AxisBuiltInUnit enumeration
linktitle: AxisBuiltInUnit enumeration
articleTitle: AxisBuiltInUnit enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisBuiltInUnit enumeration. Specifies the display units for an axis."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.charts/axisbuiltinunit/
---

## AxisBuiltInUnit enumeration

Specifies the display units for an axis.


### Members

| Name | Description |
| --- | --- |
| NONE | Specifies the values on the chart shall displayed as is. |
| CUSTOM | Specifies the values on the chart shall be divided by a user-defined divisor. This value is not supported by the new chart types of MS Office 2016. |
| BILLIONS | Specifies the values on the chart shall be divided by 1,000,000,000. |
| HUNDRED_MILLIONS | Specifies the values on the chart shall be divided by 100,000,000. |
| HUNDREDS | Specifies the values on the chart shall be divided by 100. |
| HUNDRED_THOUSANDS | Specifies the values on the chart shall be divided by 100,000. |
| MILLIONS | Specifies the values on the chart shall be divided by 1,000,000. |
| TEN_MILLIONS | Specifies the values on the chart shall be divided by 10,000,000. |
| TEN_THOUSANDS | Specifies the values on the chart shall be divided by 10,000. |
| THOUSANDS | Specifies the values on the chart shall be divided by 1,000. |
| TRILLIONS | Specifies the values on the chart shall be divided by 1,000,000,000,0000. |
| PERCENTAGE | Specifies the values on the chart shall be divided by 0.01. This value is supported only by the new chart types of MS Office 2016. |

### Examples

Shows how to manipulate the tick marks and displayed values of a chart axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SCATTER, width=450, height=250)
chart = shape.chart
self.assertEqual(1, chart.series.count)
self.assertEqual('Y-Values', chart.series[0].name)
# Set the minor tick marks of the Y-axis to point away from the plot area,
# and the major tick marks to cross the axis.
axis = chart.axis_y
axis.major_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.OUTSIDE
# Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
axis.major_unit = 10
axis.minor_unit = 1
# Set the Y-axis bounds to -10 and 20.
# This Y-axis will now display 4 major tick marks and 27 minor tick marks.
axis.scaling.minimum = aw.drawing.charts.AxisBound(value=-10)
axis.scaling.maximum = aw.drawing.charts.AxisBound(value=20)
# For the X-axis, set the major tick marks at every 10 units,
# every minor tick mark at 2.5 units.
axis = chart.axis_x
axis.major_unit = 10
axis.minor_unit = 2.5
# Configure both types of tick marks to appear inside the graph plot area.
axis.major_tick_mark = aw.drawing.charts.AxisTickMark.INSIDE
axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.INSIDE
# Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
axis.scaling.minimum = aw.drawing.charts.AxisBound(value=-10)
axis.scaling.maximum = aw.drawing.charts.AxisBound(value=30)
axis.tick_labels.alignment = aw.ParagraphAlignment.RIGHT
self.assertEqual(1, axis.tick_labels.spacing)
# Set the tick labels to display their value in millions.
axis.display_unit.unit = aw.drawing.charts.AxisBuiltInUnit.MILLIONS
# We can set a more specific value by which tick labels will display their values.
# This statement is equivalent to the one above.
axis.display_unit.custom_unit = 1000000
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisDisplayUnit.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

