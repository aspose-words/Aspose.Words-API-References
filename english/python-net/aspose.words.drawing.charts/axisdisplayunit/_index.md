---
title: AxisDisplayUnit class
linktitle: AxisDisplayUnit class
articleTitle: AxisDisplayUnit class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisDisplayUnit class. Provides access to the scaling options of the display units for the value axis"
type: docs
weight: 50
url: /python-net/aspose.words.drawing.charts/axisdisplayunit/
---

## AxisDisplayUnit class

Provides access to the scaling options of the display units for the value axis.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [AxisDisplayUnit()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [custom_unit](./custom_unit/) | Gets or sets a user-defined divisor to scale display units on the value axis. |
| [document](./document/) | Returns the document containing the parent chart. |
| [unit](./unit/) | Gets or sets the scaling value of the display units as one of the predefined values. |

### Examples

Shows how to manipulate the tick marks and displayed values of a chart axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_chart(chart_type=ChartType.SCATTER, width=450, height=250)
chart = shape.chart
self.assertEqual(1, chart.series.count)
self.assertEqual('Y-Values', chart.series[0].name)
# Set Y-axis tick marks and units
axis = chart.axis_y
axis.major_tick_mark = AxisTickMark.CROSS
axis.minor_tick_mark = AxisTickMark.OUTSIDE
axis.major_unit = 10
axis.minor_unit = 1
axis.scaling.minimum = AxisBound(value=-10)
axis.scaling.maximum = AxisBound(value=20)
# Set X-axis tick marks and units
axis = chart.axis_x
axis.major_unit = 10
axis.minor_unit = 2.5
axis.major_tick_mark = AxisTickMark.INSIDE
axis.minor_tick_mark = AxisTickMark.INSIDE
axis.scaling.minimum = AxisBound(value=-10)
axis.scaling.maximum = AxisBound(value=30)
axis.tick_labels.alignment = ParagraphAlignment.RIGHT
self.assertEqual(1, axis.tick_labels.spacing)
self.assertEqual(doc, axis.display_unit.document)
# Set display unit to millions
axis.display_unit.unit = AxisBuiltInUnit.MILLIONS
axis.display_unit.custom_unit = 1000000
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisDisplayUnit.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

