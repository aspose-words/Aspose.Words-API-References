﻿---
title: unit property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the scaling value of the display units as one of the predefined values."
type: docs
weight: 40
url: /python-net/aspose.words.drawing.charts/axisdisplayunit/unit/
---

## AxisDisplayUnit.unit property

Gets or sets the scaling value of the display units as one of the predefined values.

Default value is [AxisBuiltInUnit.NONE](../../axisbuiltinunit/#NONE). The [AxisBuiltInUnit.CUSTOM](../../axisbuiltinunit/#CUSTOM) and
[AxisBuiltInUnit.PERCENTAGE](../../axisbuiltinunit/#PERCENTAGE) values are not available in some chart types; see
[AxisBuiltInUnit](../../axisbuiltinunit/) for more information.



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
axis.tick_label_alignment = aw.ParagraphAlignment.RIGHT

self.assertEqual(1, axis.tick_label_spacing)

# Set the tick labels to display their value in millions.
axis.display_unit.unit = aw.drawing.charts.AxisBuiltInUnit.MILLIONS

# We can set a more specific value by which tick labels will display their values.
# This statement is equivalent to the one above.
axis.display_unit.custom_unit = 1000000

doc.save(ARTIFACTS_DIR + "Charts.axis_display_unit.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisDisplayUnit](../)
