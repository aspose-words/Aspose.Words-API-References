---
title: ChartXValue.from_double method
linktitle: from_double method
articleTitle: from_double method
second_title: Aspose.Words for Python
description: "ChartXValue.from_double method. Creates a [ChartXValue](../) instance of the [ChartXValueType.DOUBLE](../../chartxvaluetype/#DOUBLE) type."
type: docs
weight: 80
url: /python-net/aspose.words.drawing.charts/chartxvalue/from_double/
---

## from_double(value) {#float}

Creates a [ChartXValue](../) instance of the [ChartXValueType.DOUBLE](../../chartxvaluetype/#DOUBLE) type.



```python
def from_double(self, value: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | float |  |

### Examples

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

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartXValue](../)

