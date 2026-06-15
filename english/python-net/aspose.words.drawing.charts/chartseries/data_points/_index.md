---
title: ChartSeries.data_points property
linktitle: data_points property
articleTitle: data_points property
second_title: Aspose.Words for Python
description: "ChartSeries.data_points property. Returns a collection of formatting objects for all data points in this series."
type: docs
weight: 40
url: /python-net/aspose.words.drawing.charts/chartseries/data_points/
---

## ChartSeries.data_points property

Returns a collection of formatting objects for all data points in this series.


```python
@property
def data_points(self) -> aspose.words.drawing.charts.ChartDataPointCollection:
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
* class [ChartSeries](../)

