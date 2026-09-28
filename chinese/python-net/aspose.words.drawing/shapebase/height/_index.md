---
title: ShapeBase.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for Python
description: "ShapeBase.height property. Gets or sets the height of the containing block of the shape."
type: docs
weight: 210
url: /zh/python-net/aspose.words.drawing/shapebase/height/
---

## ShapeBase.height property

Gets or sets the height of the containing block of the shape.


```python
@property
def height(self) -> float:
    ...

@height.setter
def height(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.




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

Shows how to resize a shape with an image.

```python
# 当我们使用 "InsertImage" 方法插入图像时，构建器会缩放显示图像的形状，使得，
# 在 Microsoft Word 中以 100% 缩放查看文档时，形状会以实际大小显示图像。
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 400×400 的图像将创建一个图像大小为 300×300pt 的 ImageData 对象。
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# 如果形状的尺寸与图像数据的尺寸匹配，
# 则形状以原始大小显示图像。
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# 将形状的整体大小缩小 50%。
# 缩放因子同时作用于宽度和高度，以保持形状的比例。
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# 当您调整形状大小时，图像数据的尺寸保持不变。
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# 我们可以参考图像数据的尺寸，根据图像大小应用缩放。
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

