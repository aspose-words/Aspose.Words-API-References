---
title: ChartNumberFormat.format_code property
linktitle: format_code property
articleTitle: format_code property
second_title: Aspose.Words for Python
description: "ChartNumberFormat.format_code property. Gets or sets the format code applied to a data label."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/chartnumberformat/format_code/
---

## ChartNumberFormat.format_code property

Gets or sets the format code applied to a data label.

Number formatting is used to change the way a value appears in data label and can be used in some very creative ways.
The examples of number formats:
Number - "#,##0.00"

Currency - "\\"$\\"#,##0.00"

Time - "[$-x-systime]h:mm:ss AM/PM"

Date - "d/mm/yyyy"

Percentage - "0.00%"

Fraction - "# ?/?"

Scientific - "0.00E+00"

Text - "@"

Accounting - "_-\\"$\\"\* #,##0.00_-;-\\"$\\"\* #,##0.00_-;_-\\"$\\"\* \\"-\\"??_-;_-@_-"

Custom with color - "[Red]-#,##0.0"




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

Shows how to set formatting for chart values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_chart(aw.drawing.charts.ChartType.COLUMN, 500, 300)
chart = shape.chart

# Clear the chart's demo data series to start with a clean chart.
chart.series.clear()

# Add a custom series to the chart with categories for the X-axis,
# and large respective numeric values for the Y-axis.
chart.series.add("Aspose Test Series",
    ["Word", "PDF", "Excel", "GoogleDocs", "Note"],
    [1900000, 850000, 2100000, 600000, 1500000])

# Set the number format of the Y-axis tick labels to not group digits with commas.
chart.axis_y.number_format.format_code = "#,##0"

# This flag can override the above value and draw the number format from the source cell.
self.assertFalse(chart.axis_y.number_format.is_linked_to_source)

doc.save(ARTIFACTS_DIR + "Charts.set_number_format_to_chart_axis.docx")
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartNumberFormat](../)

