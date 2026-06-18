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

