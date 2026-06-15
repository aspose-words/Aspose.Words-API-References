---
title: ChartDataLabelCollection class
linktitle: ChartDataLabelCollection class
articleTitle: ChartDataLabelCollection class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartDataLabelCollection class. Represents a collection of [ChartDataLabel](../chartdatalabel/)"
type: docs
weight: 200
url: /python-net/aspose.words.drawing.charts/chartdatalabelcollection/
---

## ChartDataLabelCollection class

Represents a collection of [ChartDataLabel](../chartdatalabel/).
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns [ChartDataLabel](../chartdatalabel/) for the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Returns the number of [ChartDataLabel](../chartdatalabel/) in this collection. |
| [font](./font/) | Provides access to the font formatting of the data labels of the entire series. |
| [format](./format/) | Provides access to fill and line formatting of the data labels. |
| [number_format](./number_format/) | Gets an [ChartNumberFormat](../chartnumberformat/) instance allowing to set number format for the data labels of the entire series. |
| [orientation](./orientation/) | Gets or sets the text orientation of the data labels of the entire series. |
| [position](./position/) | Gets or sets the position of the data labels. |
| [rotation](./rotation/) | Gets or sets the rotation of the data labels of the entire series in degrees. |
| [separator](./separator/) | Gets or sets string separator used for the data labels of the entire series. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead. |
| [show_bubble_size](./show_bubble_size/) | Allows to specify whether bubble size is to be displayed for the data labels of the entire series. Applies only to Bubble charts. Default value is ``False``. |
| [show_category_name](./show_category_name/) | Allows to specify whether category name is to be displayed for the data labels of the entire series. Default value is ``False``. |
| [show_data_labels_range](./show_data_labels_range/) | Allows to specify whether values from data labels range to be displayed in the data labels of the entire series. Default value is ``False``. |
| [show_leader_lines](./show_leader_lines/) | Allows to specify whether data label leader lines need be shown for the data labels of the entire series. Default value is ``False``. |
| [show_legend_key](./show_legend_key/) | Allows to specify whether legend key is to be displayed for the data labels of the entire series. Default value is ``False``. |
| [show_percentage](./show_percentage/) | Allows to specify whether percentage value is to be displayed for the data labels of the entire series. Default value is ``False``. Applies only to Pie charts. |
| [show_series_name](./show_series_name/) | Returns or sets a Boolean to indicate the series name display behavior for the data labels of the entire series. ``True`` to show the series name; ``False`` to hide. By default ``False``. |
| [show_value](./show_value/) | Allows to specify whether values are to be displayed in the data labels of the entire series. Default value is ``False``. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_format()](./clear_format/#default) | Clears format of all [ChartDataLabel](../chartdatalabel/) in this collection. |

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

