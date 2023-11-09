---
title: ChartDataLabelCollection.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.font property. Provides access to the font formatting of the data labels of the entire series."
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/chartdatalabelcollection/font/
---

## ChartDataLabelCollection.font property

Provides access to the font formatting of the data labels of the entire series.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Remarks

Value defined for this property can be overridden for an individual data label with using the
[ChartDataLabel.font](../../chartdatalabel/font/) property.



### Examples

Shows how to enable and configure data labels for a chart series.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add a line chart, then clear its demo data series to start with a clean chart,
# and then set a title.
shape = builder.insert_chart(aw.drawing.charts.ChartType.LINE, 500, 300)
chart = shape.chart
chart.series.clear()
chart.title.text = "Monthly sales report"

# Insert a custom chart series with months as categories for the X-axis,
# and respective decimal amounts for the Y-axis.
series = chart.series.add("Revenue", ["January", "February", "March"], [25.611, 21.439, 33.750])

# Enable data labels, and then apply a custom number format for values displayed in the data labels.
# This format will treat displayed decimal values as millions of US Dollars.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_value = True
data_labels.number_format.format_code = "\"US$\" #,##0.000\"M\""
data_labels.font.size = 12

doc.save(ARTIFACTS_DIR + "Charts.data_label_number_format.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

