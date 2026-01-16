---
title: ChartSeriesCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.count property. Returns the number of [ChartSeries](../../chartseries/) in this collection."
type: docs
weight: 20
url: /python-net/aspose.words.drawing.charts/chartseriescollection/count/
---

## ChartSeriesCollection.count property

Returns the number of [ChartSeries](../../chartseries/) in this collection.



```python
@property
def count(self) -> int:
    ...

```

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
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# We can add a series with new values for existing categories.
# This chart will now contain four clusters of four columns.
chart.series.add('Series 4', categories, [4.4, 7.0, 3.5, 2.1])
# A chart series can also be removed by index, like this.
# This will remove one of the three demo series that came with the chart.
chart_data.remove_at(2)
self.assertFalse(any((s for s in chart_data if s.name == 'Series 3')))
# We can also clear all the chart's data at once with this method.
# When creating a new chart, this is the way to wipe all the demo data
# before we can begin working on a blank chart.
chart_data.clear()
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

