---
title: ShapeBase.local_to_parent method
linktitle: local_to_parent method
articleTitle: local_to_parent method
second_title: Aspose.Words for Python
description: "ShapeBase.local_to_parent method. Converts a value from the local coordinate space into the coordinate space of the parent shape."
type: docs
weight: 680
url: /tr/python-net/aspose.words.drawing/shapebase/local_to_parent/
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
# Bir grup şekil ekleyin ve onu aşağıdan 100 puan ve sağdan 100 puan konumlandırın
# belgenin x ve Y koordinat başlangıç noktasını.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# "LocalToParent" yöntemini kullanarak grup içindeki x ve y koordinatlarında (0, 0) noktasını belirleyin
# (100, 100) koordinatı, üst şeklin koordinat sisteminde yer alır. Grup şeklinin ebeveyni doğrudan belgedir.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# Varsayılan olarak, bir şeklin iç koordinat düzlemi sol üst köşesi (0, 0) noktasındadır,
# ve sağ alt köşesi (1000, 1000) noktasındadır. Boyutu nedeniyle grup şeklimiz 500pt x 500pt bir alanı kaplar
# belgenin düzleminde. Bu, belgenin koordinat düzleminde 1pt hareketin
# grup şeklinin koordinat düzleminde 2pt hareket anlamına geldiği anlamına gelir.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Grup şeklinin x ve y eksen başlangıç noktasını sol üst köşeden merkeze taşıyın.
# Bu, grup iç koordinatlarını belgenin koordinatlarına göre daha da kaydıracak.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Koordinat düzleminin ölçeğini değiştirmek aynı zamanda göreli konumları da etkiler.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Bu gruba bir şekil eklemek ve konumunu belgedeki bir konuma göre tanımlamak istiyorsak,
# önce grup şekli içinde belgenin konumuyla eşleşecek bir konumu doğrulamamız gerekir.
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

