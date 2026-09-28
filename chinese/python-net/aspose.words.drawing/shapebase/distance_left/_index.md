---
title: ShapeBase.distance_left property
linktitle: distance_left property
articleTitle: distance_left property
second_title: Aspose.Words for Python
description: "ShapeBase.distance_left property. Returns or sets the distance (in points) between the document text and the left edge of the shape."
type: docs
weight: 140
url: /zh/python-net/aspose.words.drawing/shapebase/distance_left/
---

## ShapeBase.distance_left property

Returns or sets the distance (in points) between the document text and the left edge of the shape.


```python
@property
def distance_left(self) -> float:
    ...

@distance_left.setter
def distance_left(self, value: float):
    ...

```

### Remarks

The default value is 1/8 inch.

Has effect only for top level shapes.




### Examples

Shows how to set the wrapping distance for a text that surrounds a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入一个矩形，并让文本紧密环绕其边界。
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=150, height=150)
shape.wrap_type = aw.drawing.WrapType.TIGHT
# 将形状与周围文本之间的最小距离设置为四周 40pt。
shape.distance_top = 40
shape.distance_bottom = 40
shape.distance_left = 40
shape.distance_right = 40
# 将形状移动更靠近页面中心，然后顺时针旋转 60 度。
shape.top = 75
shape.left = 150
shape.rotation = 60
# 添加环绕形状的文本。
builder.font.size = 24
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Coordinates.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

