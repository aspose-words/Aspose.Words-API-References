---
title: ChartDataLabelCollection.show_percentage property
linktitle: show_percentage property
articleTitle: show_percentage property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.show_percentage property. Allows to specify whether percentage value is to be displayed for the data labels of the entire series"
type: docs
weight: 110
url: /python-net/aspose.words.drawing.charts/chartdatalabelcollection/show_percentage/
---

## ChartDataLabelCollection.show_percentage property

Allows to specify whether percentage value is to be displayed for the data labels of the entire series.
Default value is ``False``. Applies only to Pie charts. 


Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.show_percentage](../../chartdatalabel/show_percentage/) property.



### Examples

Shows how to work with data labels of a pie chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

chart = builder.insert_chart(aw.drawing.charts.ChartType.PIE, 500, 300).chart

# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()

# Insert a custom chart series with a category name for each of the sectors, and their frequency table.
series = chart.series.add("Aspose Test Series",
    ["Word", "PDF", "Excel"],
    [2.7, 3.2, 0.8])

# Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_leader_lines = True
data_labels.show_legend_key = True
data_labels.show_percentage = True
data_labels.show_value = True
data_labels.separator = "; "

doc.save(ARTIFACTS_DIR + "Charts.data_labels_pie_chart.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

