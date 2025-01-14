---
title: ChartSeries.insert method
linktitle: insert method
articleTitle: insert method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeries.insert method"
type: docs
weight: 200
url: /python-net/aspose.words.drawing.charts/chartseries/insert/
---

## insert(index, x_value) {#int_chartxvalue}

Inserts the specified X value into the chart series at the specified index. If the series supports Y values
and bubble sizes, they will be empty for the X value.


```python
def insert(self, index: int, x_value: aspose.words.drawing.charts.ChartXValue):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| x_value | [ChartXValue](../../chartxvalue/) |  |

### Remarks

The corresponding data point with default formatting will be inserted into the data point collection. And,
if data labels are displayed, the corresponding data label with default formatting will be inserted too.


## insert(index, x_value, y_value) {#int_chartxvalue_chartyvalue}

Inserts the specified X and Y values into the chart series at the specified index.


```python
def insert(self, index: int, x_value: aspose.words.drawing.charts.ChartXValue, y_value: aspose.words.drawing.charts.ChartYValue):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| x_value | [ChartXValue](../../chartxvalue/) |  |
| y_value | [ChartYValue](../../chartyvalue/) |  |

### Remarks

The corresponding data point with default formatting will be inserted into the data point collection. And,
if data labels are displayed, the corresponding data label with default formatting will be inserted too.


## insert(index, x_value, y_value, bubble_size) {#int_chartxvalue_chartyvalue_float}

Inserts the specified X value, Y value and bubble size into the chart series at the specified index.


```python
def insert(self, index: int, x_value: aspose.words.drawing.charts.ChartXValue, y_value: aspose.words.drawing.charts.ChartYValue, bubble_size: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| x_value | [ChartXValue](../../chartxvalue/) |  |
| y_value | [ChartYValue](../../chartyvalue/) |  |
| bubble_size | float |  |

### Remarks

The corresponding data point with default formatting will be inserted into the data point collection. And,
if data labels are displayed, the corresponding data label with default formatting will be inserted too.


## Examples

Shows how to insert data into a chart series.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=432, height=252)
chart = shape.chart
series1 = chart.series[0]
# Clear X and Y values of the first series.
series1.clear_values()
# Populate the series with data.
series1.insert(index=0, x_value=aw.drawing.charts.ChartXValue.from_double(3))
series1.insert(index=1, x_value=aw.drawing.charts.ChartXValue.from_double(3), y_value=aw.drawing.charts.ChartYValue.from_double(10))
series1.insert(index=2, x_value=aw.drawing.charts.ChartXValue.from_double(3), y_value=aw.drawing.charts.ChartYValue.from_double(10))
series1.insert(index=3, x_value=aw.drawing.charts.ChartXValue.from_double(3), y_value=aw.drawing.charts.ChartYValue.from_double(10), bubble_size=10)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.PopulateChartWithData.docx')
```

## See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

