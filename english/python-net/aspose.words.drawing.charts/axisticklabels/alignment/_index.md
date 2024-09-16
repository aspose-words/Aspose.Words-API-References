---
title: AxisTickLabels.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "AxisTickLabels.alignment property. Gets or sets text alignment of the axis tick labels."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/axisticklabels/alignment/
---

## AxisTickLabels.alignment property

Gets or sets text alignment of the axis tick labels.


```python
@property
def alignment(self) -> aspose.words.ParagraphAlignment:
    ...

@alignment.setter
def alignment(self, value: aspose.words.ParagraphAlignment):
    ...

```

### Remarks

This property has effect only for multi-line labels.

The default value is [ParagraphAlignment.CENTER](../../../aspose.words/paragraphalignment/#CENTER).

.


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
chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel', 'GoogleDocs', 'Note'], values=[640, 320, 280, 120, 150])
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

* module [aspose.words.drawing.charts](../../)
* class [AxisTickLabels](../)

