---
title: ChartSeriesCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.clear method. Removes all [ChartSeries](../../chartseries/) from this collection."
type: docs
weight: 80
url: /python-net/aspose.words.drawing.charts/chartseriescollection/clear/
---

## clear() {#default}

Removes all [ChartSeries](../../chartseries/) from this collection.



```python
def clear(self):
    ...
```

### Examples

Shows how to add and remove series data in a chart.

```python
# Insert a column chart that will contain three series of demo data by default.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart_data = chart.series
assert chart_data.count == 3
# Print the name of every series in the chart.
for series in chart.series:
    print(series.name)
# These are the names of the categories in the chart.
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# We can add a series with new values for existing categories.
# This chart will now contain four clusters of four columns.
chart.series.add(series_name='Series 4', categories=categories, values=[4.4, 7, 3.5, 2.1])
assert chart_data.count == 4
assert chart_data[3].name == 'Series 4'
# A chart series can also be removed by index, like this.
# This will remove one of the three demo series that came with the chart.
chart_data.remove_at(2)
assert not any([s.name == 'Series 3' for s in chart_data])
assert chart_data.count == 3
assert chart_data[2].name == 'Series 4'
# We can also clear all the chart's data at once with this method.
# When creating a new chart, this is the way to wipe all the demo data
# before we can begin working on a blank chart.
chart_data.clear()
assert chart_data.count == 0
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

