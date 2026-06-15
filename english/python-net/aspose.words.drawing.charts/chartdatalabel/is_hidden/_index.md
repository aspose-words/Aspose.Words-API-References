---
title: ChartDataLabel.is_hidden property
linktitle: is_hidden property
articleTitle: is_hidden property
second_title: Aspose.Words for Python
description: "ChartDataLabel.is_hidden property. Gets/sets a flag indicating whether this label is hidden"
type: docs
weight: 40
url: /python-net/aspose.words.drawing.charts/chartdatalabel/is_hidden/
---

## ChartDataLabel.is_hidden property

Gets/sets a flag indicating whether this label is hidden.
The default value is ``False``.



```python
@property
def is_hidden(self) -> bool:
    ...

@is_hidden.setter
def is_hidden(self, value: bool):
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

