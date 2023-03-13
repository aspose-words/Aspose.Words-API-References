﻿---
title: ChartSeriesCollection class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents collection of a [ChartSeries](../chartseries/)"
type: docs
weight: 250
url: /python-net/aspose.words.drawing.charts/chartseriescollection/
---

## ChartSeriesCollection class

Represents collection of a [ChartSeries](../chartseries/).
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a [ChartSeries](../chartseries/) at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of [ChartSeries](../chartseries/) in this collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(series_name, categories, values)](./add/#str_strlist_floatlist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Bar, Column, Line and Surface charts. |
|[ add(series_name, x_values, y_values)](./add/#str_floatlist_floatlist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Scatter charts. |
|[ add(series_name, dates, values)](./add/#str_datetimelist_floatlist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Area, Radar and Stock charts. |
|[ add(series_name, x_values, y_values, bubble_sizes)](./add/#str_floatlist_floatlist_floatlist) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Bubble charts. |
|[ add_date(series_name, dates, values)](./add_date/#str_datetimelist_floatlist) |  |
|[ add_double(series_name, x_values, y_values)](./add_double/#str_floatlist_floatlist) |  |
|[ clear()](./clear/#default) | Removes all [ChartSeries](../chartseries/) from this collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a [ChartSeries](../chartseries/) at the specified index. |

### Examples

Shows how to add and remove series data in a chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a column chart that will contain three series of demo data by default.
chart_shape = builder.insert_chart(aw.drawing.charts.ChartType.COLUMN, 400, 300)
chart = chart_shape.chart

# Each series has four decimal values: one for each of the four categories.
# Four clusters of three columns will represent this data.
chart_data = chart.series

self.assertEqual(3, chart_data.count)

# Print the name of every series in the chart.
for series in chart.series:
    print(series.name)

# These are the names of the categories in the chart.
categories = ["Category 1", "Category 2", "Category 3", "Category 4"]

# We can add a series with new values for existing categories.
# This chart will now contain four clusters of four columns.
chart.series.add("Series 4", categories, [4.4, 7.0, 3.5, 2.1])

# A chart series can also be removed by index, like this.
# This will remove one of the three demo series that came with the chart.
chart_data.remove_at(2)

self.assertFalse(any(s for s in chart_data if s.name == "Series 3"))

# We can also clear all the chart's data at once with this method.
# When creating a new chart, this is the way to wipe all the demo data
# before we can begin working on a blank chart.
chart_data.clear()
```

### See Also

* module [aspose.words.drawing.charts](../)

