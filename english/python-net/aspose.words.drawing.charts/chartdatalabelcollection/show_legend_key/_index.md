---
title: ChartDataLabelCollection.show_legend_key property
linktitle: show_legend_key property
articleTitle: show_legend_key property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.show_legend_key property. Allows to specify whether legend key is to be displayed for the data labels of the entire series"
type: docs
weight: 110
url: /python-net/aspose.words.drawing.charts/chartdatalabelcollection/show_legend_key/
---

## ChartDataLabelCollection.show_legend_key property

Allows to specify whether legend key is to be displayed for the data labels of the entire series.
Default value is ``False``.



```python
@property
def show_legend_key(self) -> bool:
    ...

@show_legend_key.setter
def show_legend_key(self, value: bool):
    ...

```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.show_legend_key](../../chartdatalabel/show_legend_key/) property.



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

