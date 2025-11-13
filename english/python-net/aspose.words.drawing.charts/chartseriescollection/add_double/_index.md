---
title: ChartSeriesCollection.add_double method
linktitle: add_double method
articleTitle: add_double method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeriesCollection.add_double method"
type: docs
weight: 60
url: /python-net/aspose.words.drawing.charts/chartseriescollection/add_double/
---

## add_double(series_name, x_values, y_values) {#str_floatlist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Scatter charts.



```python
def add_double(self, series_name: str, x_values: List[float], y_values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| x_values | List[float] |  |
| y_values | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add_double(series_name, x_values) {#str_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to Histogram charts.



```python
def add_double(self, series_name: str, x_values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| x_values | List[float] |  |

### Remarks

For chart types other than Histogram, this method adds a series with empty Y values.


### Returns

Recently added [ChartSeries](../../chartseries/) object.


## Examples

Shows how to create histogram chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a Histogram chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.HISTOGRAM, width=450, height=450)
chart = shape.chart
chart.title.text = 'Avg Temperature since 1991'
# Delete default generated series.
chart.series.clear()
# Add a series.
chart.series.add_double(series_name='Avg Temperature', x_values=[51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52, 55, 52.1, 53.4, 53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7, 56.3, 55.9, 55.6])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Histogram.docx')
```

## See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

