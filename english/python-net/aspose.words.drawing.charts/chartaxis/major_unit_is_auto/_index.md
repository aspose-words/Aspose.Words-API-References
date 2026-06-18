---
title: ChartAxis.major_unit_is_auto property
linktitle: major_unit_is_auto property
articleTitle: major_unit_is_auto property
second_title: Aspose.Words for Python
description: "ChartAxis.major_unit_is_auto property. Gets or sets a flag indicating whether default distance between major tick marks shall be used."
type: docs
weight: 140
url: /python-net/aspose.words.drawing.charts/chartaxis/major_unit_is_auto/
---

## ChartAxis.major_unit_is_auto property

Gets or sets a flag indicating whether default distance between major tick marks shall be used.


```python
@property
def major_unit_is_auto(self) -> bool:
    ...

@major_unit_is_auto.setter
def major_unit_is_auto(self, value: bool):
    ...

```

### Remarks

The property has effect for time category and value axes.


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
* class [ChartAxis](../)

