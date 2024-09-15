---
title: ShapeTextOrientation enumeration
linktitle: ShapeTextOrientation enumeration
articleTitle: ShapeTextOrientation enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ShapeTextOrientation enumeration. Specifies orientation of text in shapes."
type: docs
weight: 400
url: /python-net/aspose.words.drawing/shapetextorientation/
---

## ShapeTextOrientation enumeration

Specifies orientation of text in shapes.


### Members

| Name | Description |
| --- | --- |
| HORIZONTAL | Text is arranged horizontally (lr-tb). |
| DOWNWARD | Text is rotated 90 degrees to the right to appear from top to bottom (tb-rl). |
| UPWARD | Text is rotated 90 degrees to the left to appear from bottom to top (bt-lr). |
| VERTICAL_FAR_EAST | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom (tb-rl-v). |
| VERTICAL_ROTATED_FAR_EAST | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom vertically, then left to right horizontally  (tb-lr-v). |
| WORD_ART_VERTICAL | Text is vertical, with one letter on top of the other. |
| WORD_ART_VERTICAL_RIGHT_TO_LEFT | Text is vertical, with one letter on top of the other, then right to left horizontally. |

### Examples

Shows how to change orientation and rotation for data labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
series = shape.chart.series[0]
data_labels = series.data_labels
# Show data labels.
series.has_data_labels = True
data_labels.show_value = True
data_labels.show_category_name = True
# Define data label shape.
data_labels.format.shape_type = aw.drawing.charts.ChartShapeType.UP_ARROW
data_labels.format.stroke.fill.solid(aspose.pydrawing.Color.dark_blue)
# Set data label orientation and rotation for the entire series.
data_labels.orientation = aw.drawing.ShapeTextOrientation.VERTICAL_FAR_EAST
data_labels.rotation = -45
# Change orientation and rotation of the first data label.
data_labels[0].orientation = aw.drawing.ShapeTextOrientation.HORIZONTAL
data_labels[0].rotation = 45
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LabelOrientationRotation.docx')
```

### See Also

* module [aspose.words.drawing](../)

