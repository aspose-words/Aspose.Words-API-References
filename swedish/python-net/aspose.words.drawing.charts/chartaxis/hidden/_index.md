---
title: ChartAxis.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "ChartAxis.hidden property. Gets or sets a flag indicating whether this axis is hidden or not."
type: docs
weight: 110
url: /sv/python-net/aspose.words.drawing.charts/chartaxis/hidden/
---

## ChartAxis.hidden property

Gets or sets a flag indicating whether this axis is hidden or not.


```python
@property
def hidden(self) -> bool:
    ...

@hidden.setter
def hidden(self, value: bool):
    ...

```

### Remarks

Default value is ``False``.



### Examples

Shows how to hide chart axes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=500, height=300)
chart = shape.chart
# Rensa diagrammets demo-dataserier för att börja med ett rent diagram.
chart.series.clear()
# Lägg till en anpassad serie med kategorier för X-axeln och motsvarande decimala värden för Y-axeln.
chart.series.add(series_name='AW Series 1', categories=['Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5'], values=[1.2, 0.3, 2.1, 2.9, 4.2])
# Dölj diagramaxlarna för att förenkla diagrammets utseende.
chart.axis_x.hidden = True
chart.axis_y.hidden = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.HideChartAxis.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxis](../)

