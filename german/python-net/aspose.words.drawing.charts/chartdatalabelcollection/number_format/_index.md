---
title: ChartDataLabelCollection.number_format property
linktitle: number_format property
articleTitle: number_format property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.number_format property. Gets an [ChartNumberFormat](../../chartnumberformat/) instance allowing to set number format for the data labels of the entire series."
type: docs
weight: 50
url: /de/python-net/aspose.words.drawing.charts/chartdatalabelcollection/number_format/
---

## ChartDataLabelCollection.number_format property

Gets an [ChartNumberFormat](../../chartnumberformat/) instance allowing to set number format for the data labels of the
entire series.



```python
@property
def number_format(self) -> aspose.words.drawing.charts.ChartNumberFormat:
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
* class [ChartDataLabelCollection](../)

