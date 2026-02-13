---
title: ChartTitle.orientation property
linktitle: orientation property
articleTitle: orientation property
second_title: Aspose.Words for Python
description: "ChartTitle.orientation property. Gets or sets the orientation of the chart title text."
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/charttitle/orientation/
---

## ChartTitle.orientation property

Gets or sets the orientation of the chart title text.


```python
@property
def orientation(self) -> aspose.words.drawing.ShapeTextOrientation:
    ...

@orientation.setter
def orientation(self, value: aspose.words.drawing.ShapeTextOrientation):
    ...

```

### Remarks

The default value is [ShapeTextOrientation.HORIZONTAL](../../../aspose.words.drawing/shapetextorientation/#HORIZONTAL).



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
* class [ChartTitle](../)

