---
title: ChartDataLabelCollection.separator property
linktitle: separator property
articleTitle: separator property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.separator property. Gets or sets string separator used for the data labels of the entire series"
type: docs
weight: 80
url: /python-net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---

## ChartDataLabelCollection.separator property

Gets or sets string separator used for the data labels of the entire series. 
The default is a comma, except for pie charts showing only category name and percentage, when a line break 
shall be used instead.


```python
@property
def separator(self) -> str:
    ...

@separator.setter
def separator(self, value: str):
    ...

```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.separator](../../chartdatalabel/separator/) property.



### Examples

Shows how to work with data labels of a bubble chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
chart = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BUBBLE, width=500, height=300).chart
# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()
# Add a custom series with X/Y coordinates and diameter of each of the bubbles.
series = chart.series.add(series_name='Aspose Test Series', x_values=[2.9, 3.5, 1.1, 4, 4], y_values=[1.9, 8.5, 2.1, 6, 1.5], bubble_sizes=[9, 4.5, 2.5, 8, 5])
# Enable data labels, and then modify their appearance.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_bubble_size = True
data_labels.show_category_name = True
data_labels.show_series_name = True
data_labels.separator = ' & '
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelsBubbleChart.docx')
```

Shows how to work with data labels of a pie chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
chart = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PIE, width=500, height=300).chart
# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()
# Insert a custom chart series with a category name for each of the sectors, and their frequency table.
series = chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel'], values=[2.7, 3.2, 0.8])
# Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_leader_lines = True
data_labels.show_legend_key = True
data_labels.show_percentage = True
data_labels.show_value = True
data_labels.separator = '; '
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelsPieChart.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

