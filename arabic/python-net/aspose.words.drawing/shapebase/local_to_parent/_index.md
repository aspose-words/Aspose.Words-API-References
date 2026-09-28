---
title: ShapeBase.local_to_parent method
linktitle: local_to_parent method
articleTitle: local_to_parent method
second_title: Aspose.Words for Python
description: "ShapeBase.local_to_parent method. Converts a value from the local coordinate space into the coordinate space of the parent shape."
type: docs
weight: 680
url: /ar/python-net/aspose.words.drawing/shapebase/local_to_parent/
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
# أدرج شكل مجموعة، وضعه 100 نقطة أسفل وإلى يمين
# نقطة أصل إحداثيات x و Y للمستند.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# استخدم طريقة "LocalToParent" لتحديد أن (0, 0) على إحداثيات x و y الداخلية للمجموعة
# تقع على (100, 100) من نظام إحداثيات الشكل الأب. أصل مجموعة الأشكال هو المستند نفسه.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# بشكل افتراضي، يكون الزاوية العلوية اليسرى للطائرة الإحداثية الداخلية للشكل عند (0, 0)،
# والزاوية السفلية اليمنى عند (1000, 1000). بسبب حجمها، تغطي مجموعة الأشكال مساحة 500pt × 500pt
# في مستوى المستند. هذا يعني أن حركة بمقدار 1pt على مستوى إحداثيات المستند ستترجم
# إلى حركة بمقدار 2pt على مستوى إحداثيات مجموعة الأشكال.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# انقل أصل محور x و y لمجموعة الأشكال من الزاوية العلوية اليسرى إلى المركز.
# سيؤدي ذلك إلى إزاحة إحداثيات المجموعة الداخلية بالنسبة لإحداثيات المستند أكثر من ذلك.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# تغيير مقياس الطائرة الإحداثية سيؤثر أيضًا على المواقع النسبية.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# إذا أردنا إضافة شكل إلى هذه المجموعة مع تحديد موقعه بناءً على موقع في المستند،
# سنحتاج أولاً إلى تأكيد موقع في مجموعة الأشكال يتطابق مع موقع المستند.
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

