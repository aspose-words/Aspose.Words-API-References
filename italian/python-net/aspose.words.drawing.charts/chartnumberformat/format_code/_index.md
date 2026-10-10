---
title: ChartNumberFormat.format_code property
linktitle: format_code property
articleTitle: format_code property
second_title: Aspose.Words for Python
description: "ChartNumberFormat.format_code property. Gets or sets the format code applied to a data label."
type: docs
weight: 10
url: /it/python-net/aspose.words.drawing.charts/chartnumberformat/format_code/
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
# Aggiungi un grafico a linee, quindi cancella la sua serie di dati demo per iniziare con un grafico pulito,
# e poi imposta un titolo.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
chart.series.clear()
chart.title.text = 'Monthly sales report'
# Inserisci una serie di grafico personalizzata con i mesi come categorie per l'asse X,
# e gli importi decimali corrispondenti per l'asse Y.
series = chart.series.add(series_name='Revenue', categories=['January', 'February', 'March'], values=[25.611, 21.439, 33.75])
# Abilita le etichette dei dati, quindi applica un formato numerico personalizzato per i valori visualizzati nelle etichette dei dati.
# Questo formato tratterà i valori decimali visualizzati come milioni di dollari statunitensi.
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

* module [aspose.words.drawing.charts](../../)
* class [ChartNumberFormat](../)

