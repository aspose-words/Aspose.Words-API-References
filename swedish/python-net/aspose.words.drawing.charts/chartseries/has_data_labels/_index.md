---
title: ChartSeries.has_data_labels property
linktitle: has_data_labels property
articleTitle: has_data_labels property
second_title: Aspose.Words for Python
description: "ChartSeries.has_data_labels property. Gets or sets a flag indicating whether data labels are displayed for the series."
type: docs
weight: 70
url: /sv/python-net/aspose.words.drawing.charts/chartseries/has_data_labels/
---

## ChartSeries.has_data_labels property

Gets or sets a flag indicating whether data labels are displayed for the series.


```python
@property
def has_data_labels(self) -> bool:
    ...

@has_data_labels.setter
def has_data_labels(self, value: bool):
    ...

```

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

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

