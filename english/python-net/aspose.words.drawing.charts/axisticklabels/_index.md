---
title: AxisTickLabels class
linktitle: AxisTickLabels class
articleTitle: AxisTickLabels class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisTickLabels class. Represents properties of axis tick mark labels."
type: docs
weight: 100
url: /python-net/aspose.words.drawing.charts/axisticklabels/
---

## AxisTickLabels class

Represents properties of axis tick mark labels.


### Properties

| Name | Description |
| --- | --- |
| [alignment](./alignment/) | Gets or sets text alignment of the axis tick labels. |
| [font](./font/) | Provides access to font formatting of the tick labels. |
| [is_auto_spacing](./is_auto_spacing/) | Gets or sets a flag indicating whether to use automatic interval for drawing the tick labels. |
| [offset](./offset/) | Gets or sets the distance of the tick labels from the axis. |
| [orientation](./orientation/) | Gets or sets the orientation of the tick label text. |
| [position](./position/) | Gets or sets the position of the tick labels on the axis. |
| [rotation](./rotation/) | Gets or sets the rotation of the tick labels in degrees. |
| [spacing](./spacing/) | Gets or sets the interval at which the tick labels are drawn. |

### Examples

Shows how to insert a chart and modify the appearance of its axes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=500, height=300)
chart = shape.chart
# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()
# Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
chart.series.add1(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel', 'GoogleDocs', 'Note'], values=[640, 320, 280, 120, 150])
# Chart axes have various options that can change their appearance,
# such as their direction, major/minor unit ticks, and tick marks.
x_axis = chart.axis_x
x_axis.category_type = aw.drawing.charts.AxisCategoryType.CATEGORY
x_axis.crosses = aw.drawing.charts.AxisCrosses.MINIMUM
x_axis.reverse_order = False
x_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.INSIDE
x_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
x_axis.major_unit = 10
x_axis.minor_unit = 15
x_axis.tick_labels.offset = 50
x_axis.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.LOW
x_axis.tick_labels.is_auto_spacing = False
x_axis.tick_mark_spacing = 1
self.assertEqual(doc, x_axis.document)
y_axis = chart.axis_y
y_axis.category_type = aw.drawing.charts.AxisCategoryType.AUTOMATIC
y_axis.crosses = aw.drawing.charts.AxisCrosses.MAXIMUM
y_axis.reverse_order = True
y_axis.major_tick_mark = aw.drawing.charts.AxisTickMark.INSIDE
y_axis.minor_tick_mark = aw.drawing.charts.AxisTickMark.CROSS
y_axis.major_unit = 100
y_axis.minor_unit = 20
y_axis.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.NEXT_TO_AXIS
y_axis.tick_labels.alignment = aw.ParagraphAlignment.CENTER
y_axis.tick_labels.font.color = aspose.pydrawing.Color.red
y_axis.tick_labels.spacing = 1
# Column charts do not have a Z-axis.
self.assertIsNone(chart.axis_z)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisProperties.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

