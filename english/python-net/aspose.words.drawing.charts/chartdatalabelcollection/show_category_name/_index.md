---
title: ChartDataLabelCollection.show_category_name property
linktitle: show_category_name property
articleTitle: show_category_name property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.show_category_name property. Allows to specify whether category name is to be displayed for the data labels of the entire series"
type: docs
weight: 110
url: /python-net/aspose.words.drawing.charts/chartdatalabelcollection/show_category_name/
---

## ChartDataLabelCollection.show_category_name property

Allows to specify whether category name is to be displayed for the data labels of the entire series.
Default value is ``False``.



```python
@property
def show_category_name(self) -> bool:
    ...

@show_category_name.setter
def show_category_name(self, value: bool):
    ...

```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.show_category_name](../../chartdatalabel/show_category_name/) property.



### Examples

Shows how to work with data labels of a bubble chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
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

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

