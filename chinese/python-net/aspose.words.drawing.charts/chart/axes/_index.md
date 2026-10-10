---
title: Chart.axes property
linktitle: axes property
articleTitle: axes property
second_title: Aspose.Words for Python
description: "Chart.axes property. Gets a collection of all axes of this chart."
type: docs
weight: 10
url: /zh/python-net/aspose.words.drawing.charts/chart/axes/
---

## Chart.axes property

Gets a collection of all axes of this chart.


```python
@property
def axes(self) -> aspose.words.drawing.charts.ChartAxisCollection:
    ...

```

### Examples

Shows how to work with axes collection.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=500, height=300)
chart = shape.chart
# 隐藏主 Y 轴和次 Y 轴的主要网格线。
for axis in chart.axes:
    if axis.type == aw.drawing.charts.ChartAxisType.VALUE:
        axis.has_major_gridlines = False
doc.save(file_name=ARTIFACTS_DIR + 'Charts.AxisCollection.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

