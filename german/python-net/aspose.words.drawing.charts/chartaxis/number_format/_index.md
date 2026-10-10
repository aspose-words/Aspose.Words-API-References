---
title: ChartAxis.number_format property
linktitle: number_format property
articleTitle: number_format property
second_title: Aspose.Words for Python
description: "ChartAxis.number_format property. Returns a [ChartNumberFormat](../../chartnumberformat/) object that allows defining number formats for the axis."
type: docs
weight: 200
url: /de/python-net/aspose.words.drawing.charts/chartaxis/number_format/
---

## ChartAxis.number_format property

Returns a [ChartNumberFormat](../../chartnumberformat/) object that allows defining number formats for the axis.



```python
@property
def number_format(self) -> aspose.words.drawing.charts.ChartNumberFormat:
    ...

```

### Examples

Shows how to set formatting for chart values.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=500, height=300)
chart = shape.chart
# Leeren Sie die Demo‑Datenserien des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart.series.clear()
# Fügen Sie dem Diagramm eine benutzerdefinierte Serie mit Kategorien für die X-Achse hinzu,
# und großen jeweiligen numerischen Werten für die Y-Achse.
chart.series.add(series_name='Aspose Test Series', categories=['Word', 'PDF', 'Excel', 'GoogleDocs', 'Note'], values=[1900000, 850000, 2100000, 600000, 1500000])
# Stellen Sie das Zahlenformat der Y-Achsen‑Tick‑Beschriftungen so ein, dass Ziffern nicht mit Kommas gruppiert werden.
chart.axis_y.number_format.format_code = '#,##0'
# Dieses Flag kann den obigen Wert überschreiben und das Zahlenformat aus der Quellzelle übernehmen.
self.assertFalse(chart.axis_y.number_format.is_linked_to_source)
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SetNumberFormatToChartAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

