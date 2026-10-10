---
title: ChartSeriesCollection.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.clear method. Removes all [ChartSeries](../../chartseries/) from this collection."
type: docs
weight: 80
url: /sv/python-net/aspose.words.drawing.charts/chartseriescollection/clear/
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
# Infoga ett stapeldiagram som som standard kommer att innehålla tre serier med demonstrationsdata.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart_data = chart.series
assert chart_data.count == 3
# Skriv ut namnet på varje serie i diagrammet.
for series in chart.series:
    print(series.name)
# Det här är namnen på kategorierna i diagrammet.
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
# Vi kan lägga till en serie med nya värden för befintliga kategorier.
# Detta diagram kommer nu att innehålla fyra kluster med fyra staplar.
chart.series.add(series_name='Series 4', categories=categories, values=[4.4, 7, 3.5, 2.1])
assert chart_data.count == 4
assert chart_data[3].name == 'Series 4'
# En diagramserie kan också tas bort efter index, så här.
# Detta kommer att ta bort en av de tre demonstrationsserierna som följde med diagrammet.
chart_data.remove_at(2)
assert not any([s.name == 'Series 3' for s in chart_data])
assert chart_data.count == 3
assert chart_data[2].name == 'Series 4'
# Vi kan också rensa all diagramdata på en gång med den här metoden.
# När du skapar ett nytt diagram är detta sättet att rensa all demonstrationsdata
# innan vi kan börja arbeta på ett tomt diagram.
chart_data.clear()
assert chart_data.count == 0
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

