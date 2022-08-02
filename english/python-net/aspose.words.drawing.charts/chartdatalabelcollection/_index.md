---
title: ChartDataLabelCollection class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a collection of [ChartDataLabel](../chartdatalabel/)."
type: docs
weight: 150
url: /python-net/aspose.words.drawing.charts/chartdatalabelcollection/
---

## ChartDataLabelCollection class

Represents a collection of [ChartDataLabel](../chartdatalabel/).



### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns [ChartDataLabel](../chartdatalabel/) for the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of [ChartDataLabel](../chartdatalabel/) in this collection. |
| [number_format](./number_format/) | Gets an [ChartNumberFormat](../chartnumberformat/) instance allowing to set number format for the data labels of the entire series. |
| [separator](./separator/) | Gets or sets string separator used for the data labels of the entire series.  The default is a comma, except for pie charts showing only category name and percentage, when a line break  shall be used instead. |
| [show_bubble_size](./show_bubble_size/) | Allows to specify whether bubble size is to be displayed for the data labels of the entire series. Applies only to Bubble charts.  Default value is **false**. |
| [show_category_name](./show_category_name/) | Allows to specify whether category name is to be displayed for the data labels of the entire series. Default value is **false**. |
| [show_data_labels_range](./show_data_labels_range/) | Allows to specify whether values from data labels range to be displayed in the data labels of the entire series. Default value is **false**. |
| [show_leader_lines](./show_leader_lines/) | Allows to specify whether data label leader lines need be shown for the data labels of the entire series. Default value is **false**. |
| [show_legend_key](./show_legend_key/) | Allows to specify whether legend key is to be displayed for the data labels of the entire series. Default value is **false**. |
| [show_percentage](./show_percentage/) | Allows to specify whether percentage value is to be displayed for the data labels of the entire series. Default value is **false**. Applies only to Pie charts. |
| [show_series_name](./show_series_name/) | Returns or sets a Boolean to indicate the series name display behavior for the data labels of the entire series. **True** to show the series name. **False** to hide. By default **false**. |
| [show_value](./show_value/) | Allows to specify whether values are to be displayed in the data labels of the entire series. Default value is **false**. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_format()](./clear_format/#default) | Clears format of all [ChartDataLabel](../chartdatalabel/) in this collection. |

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

