---
title: AxisTickLabels.orientation property
linktitle: orientation property
articleTitle: orientation property
second_title: Aspose.Words for Python
description: "AxisTickLabels.orientation property. Gets or sets the orientation of the tick label text."
type: docs
weight: 50
url: /python-net/aspose.words.drawing.charts/axisticklabels/orientation/
---

## AxisTickLabels.orientation property

Gets or sets the orientation of the tick label text.


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

Note that some [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/) values do not affect the orientation of tick label text
in value axes.




### Examples

Shows how to change orientation and rotation for axis tick labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a column chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
x_tick_labels = shape.chart.axis_x.tick_labels
y_tick_labels = shape.chart.axis_y.tick_labels
# Set axis tick label orientation and rotation.
x_tick_labels.orientation = aw.drawing.ShapeTextOrientation.VERTICAL_FAR_EAST
x_tick_labels.rotation = -30
y_tick_labels.orientation = aw.drawing.ShapeTextOrientation.HORIZONTAL
y_tick_labels.rotation = 45
doc.save(file_name=ARTIFACTS_DIR + 'Charts.TickLabelsOrientationRotation.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [AxisTickLabels](../)

