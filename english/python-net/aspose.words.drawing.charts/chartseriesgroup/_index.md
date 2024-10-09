---
title: ChartSeriesGroup class
linktitle: ChartSeriesGroup class
articleTitle: ChartSeriesGroup class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeriesGroup class. Represents properties of a chart series group, that is, the properties of chart series of the same type associated with the same axes."
type: docs
weight: 330
url: /python-net/aspose.words.drawing.charts/chartseriesgroup/
---

## ChartSeriesGroup class

Represents properties of a chart series group, that is, the properties of chart series of the same type
associated with the same axes.


### Remarks

Combo charts contains multiple chart series groups, with a separate group for each series type.

Also, you can create a chart series group to assign secondary axes to one or more chart series.

To learn more, visit the [
            Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [axis_group](./axis_group/) | Gets or sets the axis group to which this series group belongs. |
| [axis_x](./axis_x/) | Provides access to properties of the X axis of this series group. |
| [axis_y](./axis_y/) | Provides access to properties of the Y axis of this series group. |
| [bubble_scale](./bubble_scale/) | Gets or sets the size of the bubbles as a percentage of their default size. |
| [doughnut_hole_size](./doughnut_hole_size/) | Gets or sets the hole size of the parent doughnut chart as a percentage. |
| [first_slice_angle](./first_slice_angle/) | Gets or sets the angle, in degrees, of the first slice of the parent pie chart. |
| [gap_width](./gap_width/) | Gets or sets the percentage of gap width between chart elements. |
| [overlap](./overlap/) | Gets or sets the percentage of how much the series bars or columns overlap. |
| [second_section_size](./second_section_size/) | Gets or sets the size of the pie chart secondary section as a percentage. |
| [series](./series/) | Gets a collection of series that belong to this series group. |
| [series_type](./series_type/) | Gets the type of chart series included in this group. |

### Examples

Shows how to work with the secondary axis of chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=250)
chart = shape.chart
series = chart.series
# Delete default generated series.
series.clear()
categories = ['Category 1', 'Category 2', 'Category 3']
series.add(series_name='Series 1 of primary series group', categories=categories, values=[2, 3, 4])
series.add(series_name='Series 2 of primary series group', categories=categories, values=[5, 2, 3])
# Create an additional series group, also of the line type.
new_series_group = chart.series_groups.add(aw.drawing.charts.ChartSeriesType.LINE)
# Specify the use of secondary axes for the new series group.
new_series_group.axis_group = aw.drawing.charts.AxisGroup.SECONDARY
# Hide the secondary X axis.
new_series_group.axis_x.hidden = True
# Define title of the secondary Y axis.
new_series_group.axis_y.title.show = True
new_series_group.axis_y.title.text = 'Secondary Y axis'
# Add a series to the new series group.
series3 = new_series_group.series.add(series_name='Series of secondary series group', categories=categories, values=[13, 11, 16])
series3.format.stroke.weight = 3.5
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SecondaryAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

