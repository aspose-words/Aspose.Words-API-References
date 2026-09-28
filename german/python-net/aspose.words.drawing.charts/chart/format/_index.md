---
title: Chart.format property
linktitle: format property
articleTitle: format property
second_title: Aspose.Words for Python
description: "Chart.format property. Provides access to fill and line formatting of the chart."
type: docs
weight: 60
url: /de/python-net/aspose.words.drawing.charts/chart/format/
---

## Chart.format property

Provides access to fill and line formatting of the chart.


```python
@property
def format(self) -> aspose.words.drawing.charts.ChartFormat:
    ...

```

### Examples

Shows how to use chart formating.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
# Löschen Sie standardmäßig erzeugte Serien.
series = chart.series
series.clear()
categories = ['Category 1', 'Category 2']
series.add(series_name='Series 1', categories=categories, values=[1, 2])
series.add(series_name='Series 2', categories=categories, values=[3, 4])
# Formatieren Sie den Diagrammhintergrund.
chart.format.fill.solid(aspose.pydrawing.Color.dark_slate_gray)
# Blenden Sie Achsen‑Teilstrich‑Beschriftungen aus.
chart.axis_x.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.NONE
chart.axis_y.tick_labels.position = aw.drawing.charts.AxisTickLabelPosition.NONE
# Formatieren Sie den Diagrammtitel.
chart.title.format.fill.solid(aspose.pydrawing.Color.light_goldenrod_yellow)
# Formatieren Sie den Achsentitel.
chart.axis_x.title.show = True
chart.axis_x.title.format.fill.solid(aspose.pydrawing.Color.light_goldenrod_yellow)
# Formatieren Sie die Legende.
chart.legend.format.fill.solid(aspose.pydrawing.Color.light_goldenrod_yellow)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartFormat.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

