---
title: ChartSeries.has_data_labels property
linktitle: has_data_labels property
articleTitle: has_data_labels property
second_title: Aspose.Words for Python
description: "ChartSeries.has_data_labels property. Gets or sets a flag indicating whether data labels are displayed for the series."
type: docs
weight: 70
url: /de/python-net/aspose.words.drawing.charts/chartseries/has_data_labels/
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
# Füge ein Liniendiagramm hinzu und lösche anschließend seine Demo-Datenserie, um mit einem leeren Diagramm zu beginnen,
# und setze dann einen Titel.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
chart.series.clear()
chart.title.text = 'Monthly sales report'
# Füge eine benutzerdefinierte Diagrammserie ein, wobei Monate als Kategorien für die X‑Achse dienen,
# und entsprechende Dezimalbeträge für die Y‑Achse.
series = chart.series.add(series_name='Revenue', categories=['January', 'February', 'March'], values=[25.611, 21.439, 33.75])
# Aktiviere Datenbeschriftungen und wende anschließend ein benutzerdefiniertes Zahlenformat für die in den Datenbeschriftungen angezeigten Werte an.
# Dieses Format behandelt angezeigte Dezimalwerte als Millionen US‑Dollar.
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

