---
title: ShapeBase.top property
linktitle: top property
articleTitle: top property
second_title: Aspose.Words for Python
description: "ShapeBase.top property. Gets or sets the position of the top edge of the containing block of the shape."
type: docs
weight: 580
url: /zh/python-net/aspose.words.drawing/shapebase/top/
---

## ShapeBase.top property

Gets or sets the position of the top edge of the containing block of the shape.


```python
@property
def top(self) -> float:
    ...

@top.setter
def top(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.

Has effect only for floating shapes.




### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
# 配置形状的 \"RelativeHorizontalPosition\" 属性，以将 \"Left\" 属性的值视为形状的水平距离。
# 作为形状相对于页面左侧的水平距离，单位为点。
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
# 将形状相对于页面左侧的水平距离设置为 100。
shape.left = 100
# 以类似方式使用 \"RelativeVerticalPosition\" 属性，将形状定位在页面顶部下方 80pt。
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80
# 设置形状的高度，宽度将自动按比例缩放以保持尺寸。
shape.height = 125
self.assertEqual(125, shape.width)
# \"Bottom\" 和 \"Right\" 属性包含图像的底部和右侧边缘。
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPositionSize.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

