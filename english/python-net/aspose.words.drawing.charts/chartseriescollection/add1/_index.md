---
title: ChartSeriesCollection.add1 method
linktitle: add1 method
articleTitle: add1 method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeriesCollection.add1 method"
type: docs
weight: 40
url: /python-net/aspose.words.drawing.charts/chartseriescollection/add1/
---

## add1(series_name, categories, values) {#str_strlist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Bar, Column, Line and Surface charts.



```python
def add1(self, series_name: str, categories: List[str], values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| categories | List[str] |  |
| values | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add1(series_name, categories, values, is_subtotal) {#str_strlist_floatlist_boollist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to Waterfall charts.



```python
def add1(self, series_name: str, categories: List[str], values: List[float], is_subtotal: List[bool]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str | A name of the series to be added. |
| categories | List[str] | Category names for the X axis. |
| values | List[float] | Y-axis values. |
| is_subtotal | List[bool] | Values indicating whether the corresponding Y value is a subtotal. |

### Remarks

For chart types other than Waterfall, *isSubtotal* values are ignored.


### Returns

Recently added [ChartSeries](../../chartseries/) object.


## Examples

Shows how to create pareto chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a Pareto chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PARETO, width=450, height=450)
chart = shape.chart
chart.title.text = 'Best-Selling Car'
# Delete default generated series.
chart.series.clear()
# Add a series.
chart.series.add1(series_name='Best-Selling Car', categories=['Tesla Model Y', 'Toyota Corolla', 'Toyota RAV4', 'Ford F-Series', 'Honda CR-V'], values=[1.43, 0.91, 1.17, 0.98, 0.85])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Pareto.docx')
```

Shows how to create box and whisker chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a Box & Whisker chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BOX_AND_WHISKER, width=450, height=450)
chart = shape.chart
chart.title.text = 'Points by Years'
# Delete default generated series.
chart.series.clear()
# Add a series.
series = chart.series.add1(series_name='Points by Years', categories=['WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA'], values=[91, 80, 100, 77, 90, 104, 105, 118, 120, 101, 114, 107, 110, 60, 79, 78, 77, 102, 101, 113, 94, 93, 84, 71, 80, 103, 80, 94, 100, 101])
# Show data labels.
series.has_data_labels = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.BoxAndWhisker.docx')
```

Shows how to create waterfall chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a Waterfall chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.WATERFALL, width=450, height=450)
chart = shape.chart
chart.title.text = 'New Zealand GDP'
# Delete default generated series.
chart.series.clear()
# Add a series.
series = chart.series.add1(series_name='New Zealand GDP', categories=['2018', '2019 growth', '2020 growth', '2020', '2021 growth', '2022 growth', '2022'], values=[100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62], is_subtotal=[True, False, False, True, False, False, True])
# Show data labels.
series.has_data_labels = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Waterfall.docx')
```

## See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

