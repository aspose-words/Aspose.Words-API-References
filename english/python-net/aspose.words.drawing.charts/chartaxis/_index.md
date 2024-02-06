---
title: ChartAxis class
linktitle: ChartAxis class
articleTitle: ChartAxis class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartAxis class. Represents the axis options of the chart"
type: docs
weight: 140
url: /python-net/aspose.words.drawing.charts/chartaxis/
---

## ChartAxis class

Represents the axis options of the chart.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [axis_between_categories](./axis_between_categories/) | Gets or sets a flag indicating whether the value axis crosses the category axis between categories. |
| [base_time_unit](./base_time_unit/) | Returns or sets the smallest time unit that is represented on the time category axis. |
| [category_type](./category_type/) | Gets or sets type of the category axis. |
| [crosses](./crosses/) | Specifies how this axis crosses the perpendicular axis. |
| [crosses_at](./crosses_at/) | Specifies where on the perpendicular axis the axis crosses. |
| [display_unit](./display_unit/) | Specifies the scaling value of the display units for the value axis. |
| [document](./document/) | Returns the document containing the parent chart. |
| [format](./format/) | Provides access to line formatting of the axis and fill of the tick labels. |
| [has_major_gridlines](./has_major_gridlines/) | Gets or sets a flag indicating whether the axis has major gridlines. |
| [has_minor_gridlines](./has_minor_gridlines/) | Gets or sets a flag indicating whether the axis has minor gridlines. |
| [hidden](./hidden/) | Gets or sets a flag indicating whether this axis is hidden or not. |
| [major_tick_mark](./major_tick_mark/) | Returns or sets the major tick marks. |
| [major_unit](./major_unit/) | Returns or sets the distance between major tick marks. |
| [major_unit_is_auto](./major_unit_is_auto/) | Gets or sets a flag indicating whether default distance between major tick marks shall be used. |
| [major_unit_scale](./major_unit_scale/) | Returns or sets the scale value for major tick marks on the time category axis. |
| [minor_tick_mark](./minor_tick_mark/) | Returns or sets the minor tick marks for the axis. |
| [minor_unit](./minor_unit/) | Returns or sets the distance between minor tick marks. |
| [minor_unit_is_auto](./minor_unit_is_auto/) | Gets or sets a flag indicating whether default distance between minor tick marks shall be used. |
| [minor_unit_scale](./minor_unit_scale/) | Returns or sets the scale value for minor tick marks on the time category axis. |
| [number_format](./number_format/) | Returns a [ChartNumberFormat](../chartnumberformat/) object that allows defining number formats for the axis. |
| [reverse_order](./reverse_order/) | Returns or sets a flag indicating whether values of axis should be displayed in reverse order, i.e. from max to min. |
| [scaling](./scaling/) | Provides access to the scaling options of the axis. |
| [tick_label_alignment](./tick_label_alignment/) | Gets or sets text alignment of axis tick labels. |
| [tick_label_offset](./tick_label_offset/) | Gets or sets the distance of labels from the axis. |
| [tick_label_position](./tick_label_position/) | Returns or sets the position of the tick labels on the axis. |
| [tick_label_spacing](./tick_label_spacing/) | Gets or sets the interval, at which tick labels are drawn. |
| [tick_label_spacing_is_auto](./tick_label_spacing_is_auto/) | Gets or sets a flag indicating whether automatic interval of drawing tick labels shall be used. |
| [tick_labels](./tick_labels/) | Provides access to the properties of the axis tick mark labels. |
| [tick_mark_spacing](./tick_mark_spacing/) | Gets or sets the interval, at which tick marks are drawn. |
| [title](./title/) | Provides access to the axis title properties. |
| [type](./type/) | Returns type of the axis. |

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

* module [aspose.words.drawing.charts](../)

