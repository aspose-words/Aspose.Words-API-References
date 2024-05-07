---
title: ChartSeries class
linktitle: ChartSeries class
articleTitle: ChartSeries class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeries class. Represents chart series properties"
type: docs
weight: 310
url: /python-net/aspose.words.drawing.charts/chartseries/
---

## ChartSeries class

Represents chart series properties.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




**Interfaces:** [IChartDataPoint](../ichartdatapoint/)

### Properties

| Name | Description |
| --- | --- |
| [bubble_3d](./bubble_3d/) | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [bubble_sizes](./bubble_sizes/) | Gets a collection of bubble sizes for this chart series. |
| [data_labels](./data_labels/) | Specifies the settings for the data labels for the entire series. |
| [data_points](./data_points/) | Returns a collection of formatting objects for all data points in this series. |
| [explosion](./explosion/) | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [format](./format/) | Provides access to fill and line formatting of the series. |
| [has_data_labels](./has_data_labels/) | Gets or sets a flag indicating whether data labels are displayed for the series. |
| [invert_if_negative](./invert_if_negative/) | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [legend_entry](./legend_entry/) | Gets a legend entry for this chart series. |
| [marker](./marker/) | Specifies a data marker. Marker is automatically created when requested. |
| [name](./name/) | Gets or sets the name of the series, if name is not set explicitly it is generated using index. By default returns Series plus one based index. |
| [series_type](./series_type/) | Gets the type of this chart series. |
| [smooth](./smooth/) | Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines. |
| [x_values](./x_values/) | Gets a collection of X values for this chart series. |
| [y_values](./y_values/) | Gets a collection of Y values for this chart series. |

### Methods

| Name | Description |
| --- | --- |
|[ add(x_value)](./add/#chartxvalue) | Adds the specified X value to the chart series. If the series supports Y values and bubble sizes, they will be empty for the X value. |
|[ add(x_value, y_value)](./add/#chartxvalue_chartyvalue) | Adds the specified X and Y values to the chart series. |
|[ add(x_value, y_value, bubble_size)](./add/#chartxvalue_chartyvalue_float) | Adds the specified X value, Y value and bubble size to the chart series. |
|[ clear()](./clear/#default) | Removes all data values from the chart series. Format of all individual data points and data labels is cleared. |
|[ clear_values()](./clear_values/#default) | Removes all data values from the chart series with preserving the format of the data points and data labels. |
|[ copy_format_from(data_point_index)](./copy_format_from/#int) | Copies default data point format from the data point with the specified index. |
|[ insert(index, x_value)](./insert/#int_chartxvalue) | Inserts the specified X value into the chart series at the specified index. If the series supports Y values and bubble sizes, they will be empty for the X value. |
|[ insert(index, x_value, y_value)](./insert/#int_chartxvalue_chartyvalue) | Inserts the specified X and Y values into the chart series at the specified index. |
|[ insert(index, x_value, y_value, bubble_size)](./insert/#int_chartxvalue_chartyvalue_float) | Inserts the specified X value, Y value and bubble size into the chart series at the specified index. |
|[ remove(index)](./remove/#int) | Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index. The corresponding data point and data label are also removed. |

### Examples

Shows how to apply labels to data points in a line chart.

```python
def test_data_labels(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    chart_shape = builder.insert_chart(aw.drawing.charts.ChartType.LINE, 400, 300)
    chart = chart_shape.chart

    self.assertEqual(3, chart.series.count)
    self.assertEqual("Series 1", chart.series[0].name)
    self.assertEqual("Series 2", chart.series[1].name)
    self.assertEqual("Series 3", chart.series[2].name)

    # Apply data labels to every series in the chart.
    # These labels will appear next to each data point in the graph and display its value.
    for series in chart.series:
        self.apply_data_labels(series, 4, "000.0", ", ")
        self.assertEqual(4, series.data_labels.count)

    # Change the separator string for every data label in a series.
    for label in chart.series[0].data_labels:
        self.assertEqual(", ", label.separator)
        label.separator = " & "

    # For a cleaner looking graph, we can remove data labels individually.
    chart.series[1].data_labels[2].clear_format()

    # We can also strip an entire series of its data labels at once.
    chart.series[2].data_labels.clear_format()

    doc.save(ARTIFACTS_DIR + "Charts.data_labels.docx")

def apply_data_labels(self, series: aw.drawing.charts.ChartSeries, labels_count: int, number_format: str, separator: str):
    """Apply data labels with custom number format and separator to several data points in a series."""

    for i in range(labels_count):
        series.has_data_labels = True

        self.assertFalse(series.data_labels[i].is_visible)

        series.data_labels[i].show_category_name = True
        series.data_labels[i].show_series_name = True
        series.data_labels[i].show_value = True
        series.data_labels[i].show_leader_lines = True
        series.data_labels[i].show_legend_key = True
        series.data_labels[i].show_percentage = False
        series.data_labels[i].is_hidden = False
        self.assertFalse(series.data_labels[i].show_data_labels_range)

        series.data_labels[i].number_format.format_code = number_format
        series.data_labels[i].separator = separator

        self.assertFalse(series.data_labels[i].show_data_labels_range)
        self.assertTrue(series.data_labels[i].is_visible)
        self.assertFalse(series.data_labels[i].is_hidden)
```

### See Also

* module [aspose.words.drawing.charts](../)
* class [IChartDataPoint](../ichartdatapoint/)

