---
title: ChartSeriesCollection indexer
linktitle: ChartSeriesCollection indexer
articleTitle: ChartSeriesCollection indexer
second_title: Aspose.Words for Python
description: "ChartSeriesCollection indexer. Returns a [ChartSeries](../../chartseries/) at the specified index."
type: docs
weight: 10
url: /de/python-net/aspose.words.drawing.charts/chartseriescollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Returns a [ChartSeries](../../chartseries/) at the specified index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Remarks

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. 
For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.




### Examples

Shows how to add and remove series data in a chart.

```python
# Fügen Sie ein Säulendiagramm ein, das standardmäßig drei Serien von Beispieldaten enthält.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart_data = chart.series
assert chart_data.count == 3
# Geben Sie den Namen jeder Serie im Diagramm aus.
for series in chart.series:
    print(series.name)
# Dies sind die Namen der Kategorien im Diagramm.
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# Wir können eine Serie mit neuen Werten für vorhandene Kategorien hinzufügen.
# Dieses Diagramm wird nun vier Cluster von je vier Säulen enthalten.
chart.series.add(series_name='Series 4', categories=categories, values=[4.4, 7, 3.5, 2.1])
assert chart_data.count == 4
assert chart_data[3].name == 'Series 4'
# Eine Diagrammserie kann ebenfalls nach Index entfernt werden, wie folgt.
# Damit wird eine der drei Beispielsserien, die mit dem Diagramm geliefert wurden, entfernt.
chart_data.remove_at(2)
assert not any([s.name == 'Series 3' for s in chart_data])
assert chart_data.count == 3
assert chart_data[2].name == 'Series 4'
# Wir können außerdem alle Diagrammdaten auf einmal mit dieser Methode löschen.
# Beim Erstellen eines neuen Diagramms ist dies der Weg, alle Beispieldaten zu löschen
# bevor wir mit der Arbeit an einem leeren Diagramm beginnen können.
chart_data.clear()
assert chart_data.count == 0
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

