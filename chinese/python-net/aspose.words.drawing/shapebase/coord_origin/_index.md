---
title: ShapeBase.coord_origin property
linktitle: coord_origin property
articleTitle: coord_origin property
second_title: Aspose.Words for Python
description: "ShapeBase.coord_origin property. The coordinates at the top-left corner of the containing block of this shape."
type: docs
weight: 110
url: /zh/python-net/aspose.words.drawing/shapebase/coord_origin/
---

## ShapeBase.coord_origin property

The coordinates at the top-left corner of the containing block of this shape.


```python
@property
def coord_origin(self) -> aspose.pydrawing.Point:
    ...

@coord_origin.setter
def coord_origin(self, value: aspose.pydrawing.Point):
    ...

```

### Remarks

The default value is (0,0).




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

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```python
doc = aw.Document()
# 插入一个组合形状，并将其放置在以下位置的下方 100 点和右侧 100 点
# 文档的 x 和 Y 坐标原点。
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# 使用 "LocalToParent" 方法确定组内部 x 和 y 坐标系中的 (0, 0) 点
# 位于其父形状坐标系的 (100, 100) 位置。组合形状的父对象就是文档本身。
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# 默认情况下，形状的内部坐标平面的左上角位于 (0, 0)，
# 右下角位于 (1000, 1000)。由于尺寸原因，我们的组合形状覆盖了 500pt x 500pt 的区域
# 在文档的平面中。这意味着文档坐标平面上移动 1pt 将会转换为
# 在组合形状的坐标平面上移动 2pt。
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# 将组合形状的 x 和 y 轴原点从左上角移动到中心。
# 这将进一步使组合的内部坐标相对于文档坐标产生偏移。
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# 更改坐标平面的比例也会影响相对位置。
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# 如果我们希望在基于文档中位置定义的情况下向此组合添加形状，
# 我们需要先确认组合形状中的一个位置，使其与文档的位置匹配。
self.assertEqual(aspose.pydrawing.PointF(700, 700), group.local_to_parent(aspose.pydrawing.PointF(350, 350)))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
group.append_child(shape)
doc.first_section.body.first_paragraph.append_child(group)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.LocalToParent.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

