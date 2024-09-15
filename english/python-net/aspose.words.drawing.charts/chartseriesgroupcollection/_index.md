---
title: ChartSeriesGroupCollection class
linktitle: ChartSeriesGroupCollection class
articleTitle: ChartSeriesGroupCollection class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeriesGroupCollection class. Represents a collection of [ChartSeriesGroup](../chartseriesgroup/) objects."
type: docs
weight: 340
url: /python-net/aspose.words.drawing.charts/chartseriesgroupcollection/
---

## ChartSeriesGroupCollection class

Represents a collection of [ChartSeriesGroup](../chartseriesgroup/) objects.



### Remarks

To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/)
documentation article.



### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a [ChartSeriesGroup](../chartseriesgroup/) at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of series groups in this collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(series_type)](./add/#chartseriestype) | Adds a new series group of the specified series type to this collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a series group at the specified index. All child series will be removed from the chart. |

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

