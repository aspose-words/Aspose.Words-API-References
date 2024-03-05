---
title: ChartAxis.tick_label_spacing property
linktitle: tick_label_spacing property
articleTitle: tick_label_spacing property
second_title: Aspose.Words for Python
description: "ChartAxis.tick_label_spacing property. Gets or sets the interval, at which tick labels are drawn."
type: docs
weight: 260
url: /python-net/aspose.words.drawing.charts/chartaxis/tick_label_spacing/
---

## ChartAxis.tick_label_spacing property

Gets or sets the interval, at which tick labels are drawn.


```python
@property
def tick_label_spacing(self) -> int:
    ...

@tick_label_spacing.setter
def tick_label_spacing(self, value: int):
    ...

```

### Remarks

The property has effect for text category and series axes. It is not supported by MS Office 2016 
new charts. Valid range of a value is greater than or equal to 1.

Setting this property sets the [AxisTickLabels.is_auto_spacing](../../axisticklabels/is_auto_spacing/) property to ``False``.




### Examples

Shows how to manipulate the tick marks and displayed values of a chart axis.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.SCATTER, 450, 250)
chart = shape.chart

self.assertEqual(1, chart.series.count)
self.assertEqual("Y-Values", chart.series[0].name)

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
axis.scaling.minimum = aw.drawing.charts.AxisBound(-10)
axis.scaling.maximum = aw.drawing.charts.AxisBound(20)

# For the X-axis, set the major tick marks at every 10 units,
# every minor tick mark at 2.5 units.
axis = chart.axis_x
axis.major_unit = 10
axis.minor_unit = 2.5

# Configure both types of tick marks to appear inside the graph plot area.
axis.major_tick_mark = aw.drawing.charts.AxisTickMark.INSIDE
axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.INSIDE

# Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
axis.scaling.minimum = aw.drawing.charts.AxisBound(-10)
axis.scaling.maximum = aw.drawing.charts.AxisBound(30)
axis.tick_labels.alignment = aw.ParagraphAlignment.RIGHT

self.assertEqual(1, axis.tick_labels.spacing)

# Set the tick labels to display their value in millions.
axis.display_unit.unit = aw.drawing.charts.AxisBuiltInUnit.MILLIONS

# We can set a more specific value by which tick labels will display their values.
# This statement is equivalent to the one above.
axis.display_unit.custom_unit = 1000000

doc.save(ARTIFACTS_DIR + "Charts.axis_display_unit.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

