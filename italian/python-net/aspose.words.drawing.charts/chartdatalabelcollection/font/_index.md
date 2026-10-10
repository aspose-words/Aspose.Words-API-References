---
title: ChartDataLabelCollection.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartDataLabelCollection.font property. Provides access to the font formatting of the data labels of the entire series."
type: docs
weight: 30
url: /it/python-net/aspose.words.drawing.charts/chartdatalabelcollection/font/
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

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabelCollection](../)

