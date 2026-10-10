---
title: ChartNumberFormat class
linktitle: ChartNumberFormat class
articleTitle: ChartNumberFormat class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartNumberFormat class. Represents number formatting of the parent element"
type: docs
weight: 320
url: /it/python-net/aspose.words.drawing.charts/chartnumberformat/
---

## ChartNumberFormat class

Represents number formatting of the parent element.
To learn more, visit the [Working with Charts](https://docs.aspose.com/words/python-net/working-with-charts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [format_code](./format_code/) | Gets or sets the format code applied to a data label. |
| [is_linked_to_source](./is_linked_to_source/) | Specifies whether the format code is linked to a source cell. Default is true. |

### Examples

Shows how to set formatting for chart values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=500, height=300)
chart = shape.chart
# Cancella le serie di dati demo del grafico per iniziare con un grafico pulito.
chart.series.clear()
# Aggiungi una serie personalizzata al grafico con categorie per l'asse X,
# e grandi valori numerici rispettivi per l'asse Y.
chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel', 'GoogleDocs', 'Note'], values=[1900000, 850000, 2100000, 600000, 1500000])
# Imposta il formato numerico delle etichette dei tick dell'asse Y in modo da non raggruppare le cifre con le virgole.
chart.axis_y.number_format.format_code = '#,##0'
# Questa opzione può sovrascrivere il valore sopra e prelevare il formato numerico dalla cella di origine.
self.assertFalse(chart.axis_y.number_format.is_linked_to_source)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SetNumberFormatToChartAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

