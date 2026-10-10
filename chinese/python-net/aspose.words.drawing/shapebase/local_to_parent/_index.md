---
title: ShapeBase.local_to_parent method
linktitle: local_to_parent method
articleTitle: local_to_parent method
second_title: Aspose.Words for Python
description: "ShapeBase.local_to_parent method. Converts a value from the local coordinate space into the coordinate space of the parent shape."
type: docs
weight: 680
url: /zh/python-net/aspose.words.drawing/shapebase/local_to_parent/
---

## local_to_parent(value) {#pointf}

Converts a value from the local coordinate space into the coordinate space of the parent shape.


```python
def local_to_parent(self, value: aspose.pydrawing.PointF):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | aspose.pydrawing.PointF |  |

### Examples

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

