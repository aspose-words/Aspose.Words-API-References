---
title: ChartSeries.clear_values method
linktitle: clear_values method
articleTitle: clear_values method
second_title: Aspose.Words for Python
description: "ChartSeries.clear_values method. Removes all data values from the chart series with preserving the format of the data points and data labels."
type: docs
weight: 180
url: /python-net/aspose.words.drawing.charts/chartseries/clear_values/
---

## clear_values() {#default}

Removes all data values from the chart series with preserving the format of the data points and data labels.


```python
def clear_values(self):
    ...
```

### Examples

Shows how to populate chart series with data.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
series1 = chart.series[0]
# Clear X and Y values of the first series.
series1.clear_values()
# Populate the series with data.
series1.add(x_value=aw.drawing.charts.ChartXValue.from_double(3), y_value=aw.drawing.charts.ChartYValue.from_double(10), bubble_size=10)
series1.add(x_value=aw.drawing.charts.ChartXValue.from_double(5), y_value=aw.drawing.charts.ChartYValue.from_double(5))
series1.add(x_value=aw.drawing.charts.ChartXValue.from_double(7), y_value=aw.drawing.charts.ChartYValue.from_double(11))
series1.add(x_value=aw.drawing.charts.ChartXValue.from_double(9))
series2 = chart.series[1]
# Clear X and Y values of the second series.
series2.clear()
# Populate the series with data.
series2.add(x_value=aw.drawing.charts.ChartXValue.from_double(2), y_value=aw.drawing.charts.ChartYValue.from_double(4))
series2.add(x_value=aw.drawing.charts.ChartXValue.from_double(4), y_value=aw.drawing.charts.ChartYValue.from_double(7))
series2.add(x_value=aw.drawing.charts.ChartXValue.from_double(6), y_value=aw.drawing.charts.ChartYValue.from_double(14))
series2.add(x_value=aw.drawing.charts.ChartXValue.from_double(8), y_value=aw.drawing.charts.ChartYValue.from_double(7))
doc.save(file_name=ARTIFACTS_DIR + 'Charts.PopulateChartWithData.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

