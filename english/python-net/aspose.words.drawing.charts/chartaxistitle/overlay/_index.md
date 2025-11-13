---
title: ChartAxisTitle.overlay property
linktitle: overlay property
articleTitle: overlay property
second_title: Aspose.Words for Python
description: "ChartAxisTitle.overlay property. Determines whether other chart elements shall be allowed to overlap the title"
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/chartaxistitle/overlay/
---

## ChartAxisTitle.overlay property

Determines whether other chart elements shall be allowed to overlap the title.
The default value is ``False``.



```python
@property
def overlay(self) -> bool:
    ...

@overlay.setter
def overlay(self, value: bool):
    ...

```

### Examples

Shows how to set chart axis title.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
series_coll = chart.series
# Delete default generated series.
series_coll.clear()
series_coll.add1(series_name='AW Series 1', categories=['AW Category 1', 'AW Category 2'], values=[1, 2])
chart_axis_x_title = chart.axis_x.title
chart_axis_x_title.text = 'Categories'
chart_axis_x_title.show = True
chart_axis_y_title = chart.axis_y.title
chart_axis_y_title.text = 'Values'
chart_axis_y_title.show = True
chart_axis_y_title.overlay = True
chart_axis_y_title.font.size = 12
chart_axis_y_title.font.color = aspose.pydrawing.Color.blue
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartAxisTitle.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxisTitle](../)

