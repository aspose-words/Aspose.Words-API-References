---
title: ChartDataLabel class
linktitle: ChartDataLabel class
articleTitle: ChartDataLabel class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartDataLabel class. Represents data label on a chart point or trendline"
type: docs
weight: 190
url: /python-net/aspose.words.drawing.charts/chartdatalabel/
---

## ChartDataLabel class

Represents data label on a chart point or trendline.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Remarks

On a series, the [ChartDataLabel](./) object is a member of the [ChartDataLabelCollection](../chartdatalabelcollection/). 
The [ChartDataLabelCollection](../chartdatalabelcollection/) contains a [ChartDataLabel](./) object for each point. 



### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Provides access to the font formatting of this data label. |
| [format](./format/) | Provides access to fill and line formatting of the data label. |
| [index](./index/) | Specifies the index of the containing element.  This index shall determine which of the parent's children collection this element applies to. Default value is 0. |
| [is_hidden](./is_hidden/) | Gets/sets a flag indicating whether this label is hidden. The default value is ``False``. |
| [is_visible](./is_visible/) | Returns ``True`` if this data label has something to display. |
| [left](./left/) | Gets or sets the distance of the data label in points from the left edge of the chart or from the position specified by its [ChartDataLabel.position](./position/) property, depending on the value of the [ChartDataLabel.left_mode](./left_mode/) property. |
| [left_mode](./left_mode/) | Gets or sets the interpretation mode of the [ChartDataLabel.left](./left/) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [ChartDataLabel.position](./position/) property. |
| [number_format](./number_format/) | Returns number format of the parent element. |
| [orientation](./orientation/) | Gets or sets the orientation of the label text. |
| [position](./position/) | Gets or sets the position of the data label. |
| [rotation](./rotation/) | Gets or sets the rotation of the label in degrees. |
| [separator](./separator/) | Gets or sets string separator used for the data labels on a chart.  The default is a comma, except for pie charts showing only category name and percentage, when a line break  shall be used instead. |
| [show_bubble_size](./show_bubble_size/) | Allows to specify if bubble size is to be displayed for the data labels on a chart.  Applies only to Bubble charts.  Default value is ``False``. |
| [show_category_name](./show_category_name/) | Allows to specify if category name is to be displayed for the data labels on a chart.  Default value is ``False``. |
| [show_data_labels_range](./show_data_labels_range/) | Allows to specify if values from data labels range to be displayed in the data labels.  Default value is ``False``. |
| [show_leader_lines](./show_leader_lines/) | Allows to specify if data label leader lines need be shown.  Default value is ``False``. |
| [show_legend_key](./show_legend_key/) | Allows to specify if legend key is to be displayed for the data labels on a chart.  Default value is ``False``. |
| [show_percentage](./show_percentage/) | Allows to specify if percentage value is to be displayed for the data labels on a chart.  Default value is ``False``. |
| [show_series_name](./show_series_name/) | Returns or sets a Boolean to indicate the series name display behavior for the data labels on a chart.  ``True`` to show the series name; ``False`` to hide. By default ``False``. |
| [show_value](./show_value/) | Allows to specify if values are to be displayed in the data labels.  Default value is ``False``. |
| [top](./top/) | Gets or sets the distance of the data label in points from the top edge of the chart or from the position specified by its [ChartDataLabel.position](./position/) property, depending on the value of the [ChartDataLabel.top_mode](./top_mode/) property. |
| [top_mode](./top_mode/) | Gets or sets the interpretation mode of the [ChartDataLabel.top](./top/) property value: whether it sets the location of the data label from the top edge of the chart of from the position specified by its [ChartDataLabel.position](./position/) property. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_format()](./clear_format/#default) | Clears format of this data label. The properties are set to the default values defined in the parent data label collection. |

### Examples

Shows how to apply labels to data points in a line chart (ApplyDataLabels).

```python
@staticmethod
def _apply_data_labels(series, labels_count, number_format, separator):
    series.has_data_labels = True
    series.explosion = 40
    i = 0
    while i < labels_count:
        self.assertFalse(series.data_labels[i].is_visible)
        series.data_labels[i].show_category_name = True
        series.data_labels[i].show_series_name = True
        series.data_labels[i].show_value = True
        series.data_labels[i].show_leader_lines = True
        series.data_labels[i].show_legend_key = True
        series.data_labels[i].show_percentage = False
        self.assertFalse(series.data_labels[i].is_hidden)
        self.assertFalse(series.data_labels[i].show_data_labels_range)
        series.data_labels[i].number_format.format_code = number_format
        series.data_labels[i].separator = separator
        self.assertFalse(series.data_labels[i].show_data_labels_range)
        self.assertTrue(series.data_labels[i].is_visible)
        self.assertFalse(series.data_labels[i].is_hidden)
        i += 1
```

### See Also

* module [aspose.words.drawing.charts](../)

