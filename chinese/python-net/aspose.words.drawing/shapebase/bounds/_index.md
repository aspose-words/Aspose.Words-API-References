---
title: ShapeBase.bounds property
linktitle: bounds property
articleTitle: bounds property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds property. Gets or sets the location and size of the containing block of the shape."
type: docs
weight: 70
url: /zh/python-net/aspose.words.drawing/shapebase/bounds/
---

## ShapeBase.bounds property

Gets or sets the location and size of the containing block of the shape.


```python
@property
def bounds(self) -> aspose.pydrawing.RectangleF:
    ...

@bounds.setter
def bounds(self, value: aspose.pydrawing.RectangleF):
    ...

```

### Remarks

Ignores aspect ratio lock upon setting.


For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.




### Examples

Shows how to create and populate a group shape.

```python
doc = aw.Document()
# 创建一个组形状。组形状可以显示一组子形状节点。
# 在 Microsoft Word 中，点击组形状的边界内或其子形状之一将
# 选中该组内的所有其他子形状，并允许我们一次性缩放和移动所有形状。
group = aw.drawing.GroupShape(doc)
self.assertEqual(aw.drawing.WrapType.NONE, group.wrap_type)
# 创建一个 400pt x 400pt 的组形状，并将其放置在文档的浮动形状坐标原点。
group.bounds = aspose.pydrawing.RectangleF(0, 0, 400, 400)
# 将组的内部坐标平面大小设置为 500 x 500pt。
# 组的左上角的 x 和 y 坐标将为 (0, 0)，
# 右下角的 x 和 y 坐标将为 (500, 500)。
group.coord_size = aspose.pydrawing.Size(500, 500)
# 将组的左上角坐标设置为 (-250, -250)。
# 组的中心现在的 x 和 y 坐标值为 (0, 0)，
# 右下角将位于 (250, 250)。
group.coord_origin = aspose.pydrawing.Point(-250, -250)
# 创建一个矩形来显示此组形状的边界并将其添加到组中。
child1 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child1.width = group.coord_size.width
child1.height = group.coord_size.height
child1.left = group.coord_origin.x
child1.top = group.coord_origin.y
group.append_child(child1)
# 一旦形状成为组形状的一部分，我们可以将其作为子节点访问并进行修改。
group.get_child(aw.NodeType.SHAPE, 0, True).as_shape().stroke.dash_style = aw.drawing.DashStyle.DASH
# 创建一个小的红色星形并将其插入组中。
# 将形状与组的坐标原点对齐，我们已将其移动到中心。
child2 = aw.drawing.Shape(doc, aw.drawing.ShapeType.STAR)
child2.width = 20
child2.height = 20
child2.left = -10
child2.top = -10
child2.fill_color = aspose.pydrawing.Color.red
group.append_child(child2)
# 插入一个矩形，然后在同一位置插入一个稍小的带有图像的矩形。
# 我们添加到组中的较新形状会覆盖较旧的形状。浅蓝色矩形将部分覆盖红色星形，
# 随后带图像的形状将覆盖浅蓝色矩形，以其作为框架。
# 我们无法使用形状的 "ZOrder" 属性来操控它们在组形状内的排列。
child3 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child3.width = 250
child3.height = 250
child3.left = -250
child3.top = -250
child3.fill_color = aspose.pydrawing.Color.light_blue
group.append_child(child3)
child4 = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
child4.width = 200
child4.height = 200
child4.left = -225
child4.top = -225
group.append_child(child4)
group.get_child(aw.NodeType.SHAPE, 3, True).as_shape().image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 在组形状中插入一个文本框。设置 "Left" 属性，使文本框的右边缘
# 触及组形状的右边界。设置 "Top" 属性，使文本框位于外部
# 组形状的边界，其顶部尺寸与组形状的底部边距对齐。
child5 = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
child5.width = 200
child5.height = 50
child5.left = group.coord_size.width + group.coord_origin.x - 200
child5.top = group.coord_size.height + group.coord_origin.y
group.append_child(child5)
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(group)
builder.move_to(group.get_child(aw.NodeType.SHAPE, 4, True).as_shape().append_child(aw.Paragraph(doc)))
builder.write('Hello world!')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GroupShape.docx')
```

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

