---
title: show_bubble_size property
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to specify whether bubble size is to be displayed for the data labels of the entire series"
type: docs
weight: 60
url: /python-net/aspose.words.drawing.charts/chartdatalabelcollection/show_bubble_size/
---

## ChartDataLabelCollection.show_bubble_size property

Allows to specify whether bubble size is to be displayed for the data labels of the entire series.
Applies only to Bubble charts. 
Default value is ``False``.


Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.show_bubble_size](../../chartdatalabel/show_bubble_size/) property.



### Examples

Shows how to work with data labels of a bubble chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

chart = builder.insert_chart(aw.drawing.charts.ChartType.BUBBLE, 500, 300).chart

# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()

# Add a custom series with X/Y coordinates and diameter of each of the bubbles.
series = chart.series.add("Aspose Test Series",
    [2.9, 3.5, 1.1, 4.0, 4.0],
    [1.9, 8.5, 2.1, 6.0, 1.5],
    [9.0, 4.5, 2.5, 8.0, 5.0])

# Enable data labels, and then modify their appearance.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_bubble_size = True
data_labels.show_category_name = True
data_labels.show_series_name = True
data_labels.separator = " & "

doc.save(ARTIFACTS_DIR + "Charts.data_labels_bubble_chart.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

