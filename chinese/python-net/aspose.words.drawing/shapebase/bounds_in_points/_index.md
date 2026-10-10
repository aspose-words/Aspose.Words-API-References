---
title: ShapeBase.bounds_in_points property
linktitle: bounds_in_points property
articleTitle: bounds_in_points property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_in_points property. Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape."
type: docs
weight: 80
url: /zh/python-net/aspose.words.drawing/shapebase/bounds_in_points/
---

## ShapeBase.bounds_in_points property

Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.


```python
@property
def bounds_in_points(self) -> aspose.pydrawing.RectangleF:
    ...

```

### Remarks

The returned bounds do not include the rotation of this shape or the rotation of the parent group shape, if any.


### Examples

Shows how to verify shape containing block boundaries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.LINE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=50, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=50, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.stroke_color = aspose.pydrawing.Color.orange
# 即使该线本身在文档页面上占用的空间很小，
# 它占据一个矩形容器块，我们可以使用 "Bounds" 属性来确定其大小。
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)
# 创建一个组形状，然后使用 "Bounds" 属性设置其容器块的大小。
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(0, 100, 250, 250)
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
# 创建一个矩形，验证其边界块的大小，然后将其添加到组形状中。
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
self.assertEqual(aspose.pydrawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)
group.append_child(shape)
# 组形状的坐标平面原点位于其容器块的左上角，
# 以及右下角的 (1000, 1000) 的 x 和 y 坐标。
# 我们的组形状尺寸为 250x250pt，因此组形状坐标平面上的每 4pt
# 相当于文档正文坐标平面上的 1pt。
# 我们插入的每个形状也会按 4 倍比例缩小。
# 形状的 "BoundsInPoints" 属性的变化将反映这一点。
self.assertEqual(aspose.pydrawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)
doc.first_section.body.first_paragraph.append_child(group)
# 插入一个形状并将其放置在组形状容器块的边界之外。
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000
group.append_child(shape)
# 组形状在文档正文中的占位已增大，但容器块保持不变。
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(aspose.pydrawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Bounds.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

