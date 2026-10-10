---
title: ChartSeries.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for Python
description: "ChartSeries.format property. Provides access to fill and line formatting of the series."
type: docs
weight: 60
url: /de/python-net/aspose.words.drawing.charts/chartseries/format/
---

## ChartSeries.format property

Provides access to fill and line formatting of the series.


```python
@property
def format(self) -> aspose.words.drawing.charts.ChartFormat:
    ...

```

### Examples

Sows how to set series color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
series_coll = chart.series
# Standardmäßig generierte Serie löschen.
series_coll.clear()
# Erstelle ein Array mit Kategorienamen.
categories = ['Category 1', 'Category 2']
# Neue Serie hinzufügen. Werte‑ und Kategorien‑Arrays müssen die gleiche Größe haben.
series1 = series_coll.add(series_name='Series 1', categories=categories, values=[1, 2])
series2 = series_coll.add(series_name='Series 2', categories=categories, values=[3, 4])
series3 = series_coll.add(series_name='Series 3', categories=categories, values=[5, 6])
# Setze die Serienfarbe.
series1.format.fill.fore_color = aspose.pydrawing.Color.red
series2.format.fill.fore_color = aspose.pydrawing.Color.yellow
series3.format.fill.fore_color = aspose.pydrawing.Color.blue
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SeriesColor.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeries](../)

