---
title: ChartDataLabel.orientation property
linktitle: orientation property
articleTitle: orientation property
second_title: Aspose.Words for Python
description: "ChartDataLabel.orientation property. Gets or sets the orientation of the label text."
type: docs
weight: 90
url: /zh/python-net/aspose.words.drawing.charts/chartdatalabel/orientation/
---

## ChartDataLabel.orientation property

Gets or sets the orientation of the label text.


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

Shows how to change orientation and rotation for data labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
series = shape.chart.series[0]
data_labels = series.data_labels
# 显示数据标签。
series.has_data_labels = True
data_labels.show_value = True
data_labels.show_category_name = True
# 定义数据标签形状。
data_labels.format.shape_type = aw.drawing.charts.ChartShapeType.UP_ARROW
data_labels.format.stroke.fill.solid(aspose.pydrawing.Color.dark_blue)
# 为整个系列设置数据标签的方向和旋转。
data_labels.orientation = aw.drawing.ShapeTextOrientation.VERTICAL_FAR_EAST
data_labels.rotation = -45
# 更改第一个数据标签的方向和旋转。
data_labels[0].orientation = aw.drawing.ShapeTextOrientation.HORIZONTAL
data_labels[0].rotation = 45
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LabelOrientationRotation.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabel](../)

