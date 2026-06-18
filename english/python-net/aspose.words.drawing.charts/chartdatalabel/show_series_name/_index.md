---
title: ChartDataLabel.show_series_name property
linktitle: show_series_name property
articleTitle: show_series_name property
second_title: Aspose.Words for Python
description: "ChartDataLabel.show_series_name property. Returns or sets a Boolean to indicate the series name display behavior for the data labels on a chart"
type: docs
weight: 190
url: /python-net/aspose.words.drawing.charts/chartdatalabel/show_series_name/
---

## ChartDataLabel.show_series_name property

Returns or sets a Boolean to indicate the series name display behavior for the data labels on a chart. 
``True`` to show the series name; ``False`` to hide. By default ``False``.



```python
@property
def show_series_name(self) -> bool:
    ...

@show_series_name.setter
def show_series_name(self, value: bool):
    ...

```

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

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabel](../)

