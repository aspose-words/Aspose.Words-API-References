---
title: ChartXValue class
linktitle: ChartXValue class
articleTitle: ChartXValue class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartXValue class. Represents an X value for a chart series."
type: docs
weight: 410
url: /python-net/aspose.words.drawing.charts/chartxvalue/
---

## ChartXValue class

Represents an X value for a chart series.


### Remarks

This class contains a number of static methods for creating an X value of a particular type. The
[ChartXValue.value_type](./value_type/) property allows you to determine the type of an existing X value.

All non-null X values of a chart series must be of the same [ChartXValueType](../chartxvaluetype/) type.




### Properties

| Name | Description |
| --- | --- |
| [date_time_value](./date_time_value/) | Gets the stored datetime value. |
| [double_value](./double_value/) | Gets the stored numeric value. |
| [multilevel_value](./multilevel_value/) | Gets the stored multilevel value. |
| [string_value](./string_value/) | Gets the stored string value. |
| [time_value](./time_value/) | Gets the stored time value. |
| [value_type](./value_type/) | Gets the type of the X value stored in the object. |

### Methods

| Name | Description |
| --- | --- |
|[ from_date_time(value)](./from_date_time/#datetime) | Creates a [ChartXValue](./) instance of the [ChartXValueType.DATE_TIME](../chartxvaluetype/#DATE_TIME) type. |
|[ from_double(value)](./from_double/#float) | Creates a [ChartXValue](./) instance of the [ChartXValueType.DOUBLE](../chartxvaluetype/#DOUBLE) type. |
|[ from_multilevel_value(value)](./from_multilevel_value/#chartmultilevelvalue) | Creates a [ChartXValue](./) instance of the [ChartXValueType.MULTILEVEL](../chartxvaluetype/#MULTILEVEL) type. |
|[ from_string(value)](./from_string/#str) | Creates a [ChartXValue](./) instance of the [ChartXValueType.STRING](../chartxvaluetype/#STRING) type. |
|[ from_time_span(value)](./from_time_span/#timespan) | Creates a [ChartXValue](./) instance of the [ChartXValueType.TIME](../chartxvaluetype/#TIME) type. |

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

* module [aspose.words.drawing.charts](../)

