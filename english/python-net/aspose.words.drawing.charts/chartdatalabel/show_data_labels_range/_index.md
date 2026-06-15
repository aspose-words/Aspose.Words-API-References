---
title: ChartDataLabel.show_data_labels_range property
linktitle: show_data_labels_range property
articleTitle: show_data_labels_range property
second_title: Aspose.Words for Python
description: "ChartDataLabel.show_data_labels_range property. Allows to specify if values from data labels range to be displayed in the data labels"
type: docs
weight: 150
url: /python-net/aspose.words.drawing.charts/chartdatalabel/show_data_labels_range/
---

## ChartDataLabel.show_data_labels_range property

Allows to specify if values from data labels range to be displayed in the data labels. 
Default value is ``False``.



```python
@property
def show_data_labels_range(self) -> bool:
    ...

@show_data_labels_range.setter
def show_data_labels_range(self, value: bool):
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

