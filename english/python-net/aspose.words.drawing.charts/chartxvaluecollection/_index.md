---
title: ChartXValueCollection class
linktitle: ChartXValueCollection class
articleTitle: ChartXValueCollection class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartXValueCollection class. Represents a collection of X values for a chart series."
type: docs
weight: 420
url: /python-net/aspose.words.drawing.charts/chartxvaluecollection/
---

## ChartXValueCollection class

Represents a collection of X values for a chart series.


### Remarks

All items of the collection other than **null** must have the same [ChartXValue.value_type](../chartxvalue/value_type/).

The collection allows only changing X values. To add or insert new values to a chart series, or remove values,
the appropriate methods of the [ChartSeries](../chartseries/) class can be used.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets the X value at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of items in this collection. |
| [format_code](./format_code/) | Gets or sets the format code applied to the X values. |

### Examples

Shows how to get chart series data.

```python
doc = aw.Document()
builder = aw.DocumentBuilder()
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
series = chart.series[0]
min_value = 1.7976931348623157e+308
min_value_index = 0
max_value = -1.7976931348623157e+308
max_value_index = 0
i = 0
while i < series.y_values.count:
    # Clear individual format of all data points.
    # Data points and data values are one-to-one in column charts.
    series.data_points[i].clear_format()
    # Get Y value.
    y_value = series.y_values[i].double_value
    if y_value < min_value:
        min_value = y_value
        min_value_index = i
    if y_value > max_value:
        max_value = y_value
        max_value_index = i
    i += 1
# Change colors of the max and min values.
series.data_points[min_value_index].format.fill.fore_color = aspose.pydrawing.Color.red
series.data_points[max_value_index].format.fill.fore_color = aspose.pydrawing.Color.green
doc.save(file_name=ARTIFACTS_DIR + 'Charts.GetChartSeriesData.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)
* method [ChartSeries.add()](../chartseries/add/#chartxvalue_chartyvalue)
* method [ChartSeries.add()](../chartseries/add/#chartxvalue_chartyvalue_float)
* method [ChartSeries.insert()](../chartseries/insert/#int_chartxvalue_chartyvalue)
* method [ChartSeries.insert()](../chartseries/insert/#int_chartxvalue_chartyvalue_float)
* method [ChartSeries.remove()](../chartseries/remove/#int)

