---
title: ChartNumberFormat.format_code property
linktitle: format_code property
articleTitle: format_code property
second_title: Aspose.Words for Python
description: "ChartNumberFormat.format_code property. Gets or sets the format code applied to a data label."
type: docs
weight: 10
url: /sv/python-net/aspose.words.drawing.charts/chartnumberformat/format_code/
---

## ChartNumberFormat.format_code property

Gets or sets the format code applied to a data label.


```python
@property
def format_code(self) -> str:
    ...

@format_code.setter
def format_code(self, value: str):
    ...

```

### Remarks

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
builder = aw.DocumentBuilder(doc=doc)
# Lägg till ett linjediagram, rensa sedan dess demodata-serier för att börja med ett rent diagram,
# och sätt sedan en titel.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
chart.series.clear()
chart.title.text = 'Monthly sales report'
# Infoga en anpassad diagramserie med månader som kategorier för X-axeln,
# och respektive decimala belopp för Y-axeln.
series = chart.series.add(series_name='Revenue', categories=['January', 'February', 'March'], values=[25.611, 21.439, 33.75])
# Aktivera datalabels, och applicera sedan ett anpassat talformat för värden som visas i datalabels.
# Detta format kommer att behandla visade decimala värden som miljoner US-dollar.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_value = True
data_labels.number_format.format_code = '"US$" #,##0.000"M"'
data_labels.font.size = 12
doc.save(file_name=ARTIFACTS_DIR + 'Charts.DataLabelNumberFormat.docx')
```

Shows how to set formatting for chart values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=500, height=300)
chart = shape.chart
# Rensa diagrammets demo-dataserier för att börja med ett rent diagram.
chart.series.clear()
# Lägg till en anpassad serie i diagrammet med kategorier för X-axeln,
# och stora respektive numeriska värden för Y-axeln.
chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel', 'GoogleDocs', 'Note'], values=[1900000, 850000, 2100000, 600000, 1500000])
# Ställ in talformatet för Y-axelns tick-etiketter så att siffror inte grupperas med kommatecken.
chart.axis_y.number_format.format_code = '#,##0'
# Denna flagga kan åsidosätta ovanstående värde och hämta talformatet från källcellen.
self.assertFalse(chart.axis_y.number_format.is_linked_to_source)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SetNumberFormatToChartAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartNumberFormat](../)

