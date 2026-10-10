---
title: AxisGroup enumeration
linktitle: AxisGroup enumeration
articleTitle: AxisGroup enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.AxisGroup enumeration. Represents a type of a chart axis group."
type: docs
weight: 60
url: /de/python-net/aspose.words.drawing.charts/axisgroup/
---

## AxisGroup enumeration

Represents a type of a chart axis group.


### Members

| Name | Description |
| --- | --- |
| PRIMARY | Specifies the primary axis group. |
| SECONDARY | Specifies the secondary axis group. |

### Examples

Shows how to work with the secondary axis of chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=250)
chart = shape.chart
series = chart.series
# Standardmäßig generierte Serie löschen.
series.clear()
categories = ['Category 1', 'Category 2', 'Category 3']
series.add(series_name='Series 1 of primary series group', categories=categories, values=[2, 3, 4])
series.add(series_name='Series 2 of primary series group', categories=categories, values=[5, 2, 3])
# Erstellen Sie eine zusätzliche Seriengruppe, ebenfalls vom Linientyp.
new_series_group = chart.series_groups.add(aw.drawing.charts.ChartSeriesType.LINE)
# Geben Sie die Verwendung sekundärer Achsen für die neue Seriengruppe an.
new_series_group.axis_group = aw.drawing.charts.AxisGroup.SECONDARY
# Blenden Sie die sekundäre X‑Achse aus.
new_series_group.axis_x.hidden = True
# Definieren Sie den Titel der sekundären Y‑Achse.
new_series_group.axis_y.title.show = True
new_series_group.axis_y.title.text = 'Secondary Y axis'
self.assertEqual(aw.drawing.charts.ChartSeriesType.LINE, new_series_group.series_type)
# Fügen Sie der neuen Seriengruppe eine Serie hinzu.
series3 = new_series_group.series.add(series_name='Series of secondary series group', categories=categories, values=[13, 11, 16])
series3.format.stroke.weight = 3.5
doc.save(file_name=ARTIFACTS_DIR + 'Charts.SecondaryAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../)

