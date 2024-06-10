---
title: ChartAxisTitle.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartAxisTitle.font property. Provides access to the font formatting of the axis title."
type: docs
weight: 10
url: /python-net/aspose.words.drawing.charts/chartaxistitle/font/
---

## ChartAxisTitle.font property

Provides access to the font formatting of the axis title.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Examples

Shows how to set chart axis title.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
series_coll = chart.series
# Delete default generated series.
series_coll.clear()
series_coll.add(series_name='AW Series 1', categories=['AW Category 1', 'AW Category 2'], values=[1, 2])
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

