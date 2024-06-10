---
title: ChartSeries.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeries.add method"
type: docs
weight: 160
url: /python-net/aspose.words.drawing.charts/chartseries/add/
---

## add(x_value) {#chartxvalue}

Adds the specified X value to the chart series. If the series supports Y values and bubble sizes, they will
be empty for the X value.


```python
def add(self, x_value: aspose.words.drawing.charts.ChartXValue):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| x_value | [ChartXValue](../../chartxvalue/) |  |

## add(x_value, y_value) {#chartxvalue_chartyvalue}

Adds the specified X and Y values to the chart series.


```python
def add(self, x_value: aspose.words.drawing.charts.ChartXValue, y_value: aspose.words.drawing.charts.ChartYValue):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| x_value | [ChartXValue](../../chartxvalue/) |  |
| y_value | [ChartYValue](../../chartyvalue/) |  |

## add(x_value, y_value, bubble_size) {#chartxvalue_chartyvalue_float}

Adds the specified X value, Y value and bubble size to the chart series.


```python
def add(self, x_value: aspose.words.drawing.charts.ChartXValue, y_value: aspose.words.drawing.charts.ChartYValue, bubble_size: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| x_value | [ChartXValue](../../chartxvalue/) |  |
| y_value | [ChartYValue](../../chartyvalue/) |  |
| bubble_size | float |  |

## Examples

Shows how to populate chart series with data.

```python
doc = aw.Document()
builder = aw.DocumentBuilder()
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
series1 = chart.series[0]
# Clear X and Y values of the first series.
series1.clear_values()
# Populate the series with data.
series1.add(x_value=aw.drawing.charts.ChartXValue.from_double(3), y_value=aw.drawing.charts.ChartYValue.from_double(10))
series1.add(x_value=aw.drawing.charts.ChartXValue.from_double(5), y_value=aw.drawing.charts.ChartYValue.from_double(5))
series1.add(x_value=aw.drawing.charts.ChartXValue.from_double(7), y_value=aw.drawing.charts.ChartYValue.from_double(11))
series1.add(x_value=aw.drawing.charts.ChartXValue.from_double(9), y_value=aw.drawing.charts.ChartYValue.from_double(17))
series2 = chart.series[1]
# Clear X and Y values of the second series.
series2.clear_values()
# Populate the series with data.
series2.add(x_value=aw.drawing.charts.ChartXValue.from_double(2), y_value=aw.drawing.charts.ChartYValue.from_double(4))
series2.add(x_value=aw.drawing.charts.ChartXValue.from_double(4), y_value=aw.drawing.charts.ChartYValue.from_double(7))
series2.add(x_value=aw.drawing.charts.ChartXValue.from_double(6), y_value=aw.drawing.charts.ChartYValue.from_double(14))
series2.add(x_value=aw.drawing.charts.ChartXValue.from_double(8), y_value=aw.drawing.charts.ChartYValue.from_double(7))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.PopulateChartWithData.docx')
```

Shows how to add/remove chart data values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder()
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
department_1_series = chart.series[0]
department_2_series = chart.series[1]
# Remove the first value in the both series.
department_1_series.remove(0)
department_2_series.remove(0)
# Add new values to the both series.
new_x_category = aw.drawing.charts.ChartXValue.from_string('Q1, 2023')
department_1_series.add(x_value=new_x_category, y_value=aw.drawing.charts.ChartYValue.from_double(10.3))
department_2_series.add(x_value=new_x_category, y_value=aw.drawing.charts.ChartYValue.from_double(5.7))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartDataValues.docx')
```

## See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

