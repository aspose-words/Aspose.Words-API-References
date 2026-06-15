---
title: AxisDisplayUnit.unit property
linktitle: unit property
articleTitle: unit property
second_title: Aspose.Words for Python
description: "AxisDisplayUnit.unit property. Gets or sets the scaling value of the display units as one of the predefined values."
type: docs
weight: 40
url: /python-net/aspose.words.drawing.charts/axisdisplayunit/unit/
---

## AxisDisplayUnit.unit property

Gets or sets the scaling value of the display units as one of the predefined values.


```python
@property
def unit(self) -> aspose.words.drawing.charts.AxisBuiltInUnit:
    ...

@unit.setter
def unit(self, value: aspose.words.drawing.charts.AxisBuiltInUnit):
    ...

```

### Remarks

Default value is [AxisBuiltInUnit.NONE](../../axisbuiltinunit/#NONE). The [AxisBuiltInUnit.CUSTOM](../../axisbuiltinunit/#CUSTOM) and
[AxisBuiltInUnit.PERCENTAGE](../../axisbuiltinunit/#PERCENTAGE) values are not available in some chart types; see
[AxisBuiltInUnit](../../axisbuiltinunit/) for more information.



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

* module [aspose.words.drawing.charts](../../)
* class [AxisDisplayUnit](../)

