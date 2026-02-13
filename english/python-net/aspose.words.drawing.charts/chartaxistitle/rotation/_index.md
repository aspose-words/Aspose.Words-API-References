---
title: ChartAxisTitle.rotation property
linktitle: rotation property
articleTitle: rotation property
second_title: Aspose.Words for Python
description: "ChartAxisTitle.rotation property. Gets or sets the rotation of the axis title in degrees."
type: docs
weight: 50
url: /python-net/aspose.words.drawing.charts/chartaxistitle/rotation/
---

## ChartAxisTitle.rotation property

Gets or sets the rotation of the axis title in degrees.


```python
@property
def rotation(self) -> int:
    ...

@rotation.setter
def rotation(self, value: int):
    ...

```

### Remarks

The range of acceptable values is from -180 to 180 inclusive.


### Examples

Shows how to set orientation and rotation of chart and axis titles.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=400, height=300)
chart = chart_shape.chart
chart.title.text = 'Sample Chart'
chart.title.orientation = aw.drawing.ShapeTextOrientation.HORIZONTAL
chart.title.rotation = 90
# Before setting title properties, make sure that this title will be displayed.
chart.axis_x.title.show = True
chart.axis_x.title.text = 'X Axis'
chart.axis_x.title.orientation = aw.drawing.ShapeTextOrientation.HORIZONTAL
chart.axis_x.title.rotation = -90
doc.save(file_name=ARTIFACTS_DIR + 'Charts.TitleOrientation.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartAxisTitle](../)

