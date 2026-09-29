---
title: ChartSeriesCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.clear method. Removes all [ChartSeries](../../chartseries/) from this collection."
type: docs
weight: 80
url: /it/python-net/aspose.words.drawing.charts/chartseriescollection/clear/
---

## clear() {#default}

Removes all [ChartSeries](../../chartseries/) from this collection.



```python
def clear(self):
    ...
```

### Examples

Shows how to add and remove series data in a chart.

```python
# Inserisci un grafico a colonne che conterrà tre serie di dati dimostrativi per impostazione predefinita.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart_data = chart.series
assert chart_data.count == 3
# Stampa il nome di ogni serie nel grafico.
for series in chart.series:
    print(series.name)
# Questi sono i nomi delle categorie nel grafico.
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# Possiamo aggiungere una serie con nuovi valori per le categorie esistenti.
# Questo grafico conterrà ora quattro gruppi di quattro colonne.
chart.series.add(series_name='Series 4', categories=categories, values=[4.4, 7, 3.5, 2.1])
assert chart_data.count == 4
assert chart_data[3].name == 'Series 4'
# Una serie del grafico può anche essere rimossa per indice, così.
# Questo rimuoverà una delle tre serie dimostrative incluse nel grafico.
chart_data.remove_at(2)
assert not any([s.name == 'Series 3' for s in chart_data])
assert chart_data.count == 3
assert chart_data[2].name == 'Series 4'
# Possiamo anche cancellare tutti i dati del grafico in una volta con questo metodo.
# Quando si crea un nuovo grafico, questo è il modo per cancellare tutti i dati dimostrativi
# prima di poter iniziare a lavorare su un grafico vuoto.
chart_data.clear()
assert chart_data.count == 0
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

