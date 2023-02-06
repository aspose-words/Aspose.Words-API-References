---
title: ChartDataLabel class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents data label on a chart point or trendline"
type: docs
weight: 140
url: /python-net/aspose.words.drawing.charts/chartdatalabel/
---

## ChartDataLabel class

Represents data label on a chart point or trendline.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




On a series, the [ChartDataLabel](./) object is a member of the [ChartDataLabelCollection](../chartdatalabelcollection/). 
The [ChartDataLabelCollection](../chartdatalabelcollection/) contains a [ChartDataLabel](./) object for each point. 



### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the font formatting of this data label. |
| [index](./index/) | Specifies the index of the containing element.  This index shall determine which of the parent's children collection this element applies to. Default value is 0. |
| [is_hidden](./is_hidden/) | Gets/sets a flag indicating whether this label is hidden. The default value is ``False``. |
| [is_visible](./is_visible/) | Returns ``True`` if this data label has something to display. |
| [number_format](./number_format/) | Returns number format of the parent element. |
| [separator](./separator/) | Gets or sets string separator used for the data labels on a chart.  The default is a comma, except for pie charts showing only category name and percentage, when a line break  shall be used instead. |
| [show_bubble_size](./show_bubble_size/) | Allows to specify if bubble size is to be displayed for the data labels on a chart.  Applies only to Bubble charts.  Default value is ``False``. |
| [show_category_name](./show_category_name/) | Allows to specify if category name is to be displayed for the data labels on a chart.  Default value is ``False``. |
| [show_data_labels_range](./show_data_labels_range/) | Allows to specify if values from data labels range to be displayed in the data labels.  Default value is ``False``. |
| [show_leader_lines](./show_leader_lines/) | Allows to specify if data label leader lines need be shown.  Default value is ``False``. |
| [show_legend_key](./show_legend_key/) | Allows to specify if legend key is to be displayed for the data labels on a chart.  Default value is ``False``. |
| [show_percentage](./show_percentage/) | Allows to specify if percentage value is to be displayed for the data labels on a chart.  Default value is ``False``. |
| [show_series_name](./show_series_name/) | Returns or sets a Boolean to indicate the series name display behavior for the data labels on a chart.  ``True`` to show the series name; ``False`` to hide. By default ``False``. |
| [show_value](./show_value/) | Allows to specify if values are to be displayed in the data labels.  Default value is ``False``. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_format()](./clear_format/#default) | Clears format of this data label. The properties are set to the default values defined in the parent data label collection. |

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

