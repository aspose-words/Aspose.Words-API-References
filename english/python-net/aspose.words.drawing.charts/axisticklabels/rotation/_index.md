---
title: AxisTickLabels.rotation property
linktitle: rotation property
articleTitle: rotation property
second_title: Aspose.Words for Python
description: "AxisTickLabels.rotation property. Gets or sets the rotation of the tick labels in degrees."
type: docs
weight: 70
url: /python-net/aspose.words.drawing.charts/axisticklabels/rotation/
---

## AxisTickLabels.rotation property

Gets or sets the rotation of the tick labels in degrees.


```python
@property
def rotation(self) -> int:
    ...

@rotation.setter
def rotation(self, value: int):
    ...

```

### Remarks

The range of acceptable values is from -180 to 180 inclusive. The default value is 0.


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

