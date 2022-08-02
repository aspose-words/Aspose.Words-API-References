---
title: axis_y property
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides access to properties of the Y axis of the chart."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.charts/chart/axis_y/
---

## Chart.axis_y property

Provides access to properties of the Y axis of the chart.


### Examples

Shows how to insert a chart and modify the appearance of its axes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.COLUMN, 500, 300)
chart = shape.chart

# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()

# Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
chart.series.add("Aspose Test Series",
    ["Word", "PDF", "Excel", "GoogleDocs", "Note"],
    [640, 320, 280, 120, 150])

# Chart axes have various options that can change their appearance,
# such as their direction, major/minor unit ticks, and tick marks.
x_axis = chart.axis_x
x_axis.category_type = aw.drawing.charts.AxisCategoryType.CATEGORY
x_axis.crosses = aw.drawing.charts.AxisCrosses.MINIMUM
x_axis.reverse_order = False
x_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.INSIDE
x_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
x_axis.major_unit = 10.0
x_axis.minor_unit = 15.0
x_axis.tick_label_offset = 50
x_axis.tick_label_position = aw.drawing.charts.AxisTickLabelPosition.LOW
x_axis.tick_label_spacing_is_auto = False
x_axis.tick_mark_spacing = 1

y_axis = chart.axis_y
y_axis.category_type = aw.drawing.charts.AxisCategoryType.AUTOMATIC
y_axis.crosses = aw.drawing.charts.AxisCrosses.MAXIMUM
y_axis.reverse_order = True
y_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.INSIDE
y_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
y_axis.major_unit = 100.0
y_axis.minor_unit = 20.0
y_axis.tick_label_position = aw.drawing.charts.AxisTickLabelPosition.NEXT_TO_AXIS

# Column charts do not have a Z-axis.
self.assertIsNone(chart.axis_z)

doc.save(ARTIFACTS_DIR + "Charts.axis_properties.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

