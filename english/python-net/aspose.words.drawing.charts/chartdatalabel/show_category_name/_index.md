---
title: ChartDataLabel.show_category_name property
linktitle: show_category_name property
articleTitle: show_category_name property
second_title: Aspose.Words for Python
description: "ChartDataLabel.show_category_name property. Allows to specify if category name is to be displayed for the data labels on a chart"
type: docs
weight: 90
url: /python-net/aspose.words.drawing.charts/chartdatalabel/show_category_name/
---

## ChartDataLabel.show_category_name property

Allows to specify if category name is to be displayed for the data labels on a chart. 
Default value is ``False``.



```python
@property
def show_category_name(self) -> bool:
    ...

@show_category_name.setter
def show_category_name(self, value: bool):
    ...

```

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

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabel](../)

