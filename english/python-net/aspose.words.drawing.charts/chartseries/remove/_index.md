---
title: ChartSeries.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "ChartSeries.remove method. Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index"
type: docs
weight: 210
url: /python-net/aspose.words.drawing.charts/chartseries/remove/
---

## remove(index) {#int}

Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index.
The corresponding data point and data label are also removed.


```python
def remove(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

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

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

