---
title: ShapeBase.coord_size property
linktitle: coord_size property
articleTitle: coord_size property
second_title: Aspose.Words for Python
description: "ShapeBase.coord_size property. The width and height of the coordinate space inside the containing block of this shape."
type: docs
weight: 120
url: /ar/python-net/aspose.words.drawing/shapebase/coord_size/
---

## ShapeBase.coord_size property

The width and height of the coordinate space inside the containing block of this shape.


```python
@property
def coord_size(self) -> aspose.pydrawing.Size:
    ...

@coord_size.setter
def coord_size(self, value: aspose.pydrawing.Size):
    ...

```

### Remarks

The default value is (1000, 1000).




### Examples

Shows how to create and populate a group shape.

```python
doc = aw.Document()
# أنشئ شكل مجموعة. يمكن لشكل المجموعة عرض مجموعة من عقد الأشكال الفرعية.
# في Microsoft Word، النقر داخل حدود شكل المجموعة أو على أحد الأشكال الفرعية داخل مجموعة الشكل سيؤدي إلى
# تحديد جميع الأشكال الفرعية الأخرى داخل هذه المجموعة والسماح لنا بتكبير وتحريك جميع الأشكال مرة واحدة.
group = aw.drawing.GroupShape(doc)
self.assertEqual(aw.drawing.WrapType.NONE, group.wrap_type)
# أنشئ شكل مجموعة بحجم 400pt × 400pt وضعه عند أصل إحداثيات الشكل العائم في المستند.
group.bounds = aspose.pydrawing.RectangleF(0, 0, 400, 400)
# اضبط حجم مستوى الإحداثيات الداخلي للمجموعة إلى 500 × 500pt.
# زاوية المجموعة العلوية اليسرى ستحمل إحداثيات x و y بقيمة (0, 0)،
# والزاوية السفلية اليمنى ستحمل إحداثيات x و y بقيمة (500, 500).
group.coord_size = aspose.pydrawing.Size(500, 500)
# اضبط إحداثيات الزاوية العلوية اليسرى للمجموعة إلى (-250, -250).
# مركز المجموعة سيصبح الآن لديه إحداثيات x و y بقيمة (0, 0)،
# والزاوية السفلية اليمنى ستكون عند (250, 250).
group.coord_origin = aspose.pydrawing.Point(-250, -250)
# أنشئ مستطيلًا يعرض حدود شكل المجموعة هذا وأضفه إلى المجموعة.
child1 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child1.width = group.coord_size.width
child1.height = group.coord_size.height
child1.left = group.coord_origin.x
child1.top = group.coord_origin.y
group.append_child(child1)
# بمجرد أن يصبح الشكل جزءًا من شكل مجموعة، يمكننا الوصول إليه كعقدة فرعية ثم تعديلها.
group.get_child(aw.NodeType.SHAPE, 0, True).as_shape().stroke.dash_style = aw.drawing.DashStyle.DASH
# أنشئ نجمة حمراء صغيرة وأدرجها في المجموعة.
# حاذِ الشكل مع أصل إحداثيات المجموعة، الذي نقلناه إلى المركز.
child2 = aw.drawing.Shape(doc, aw.drawing.ShapeType.STAR)
child2.width = 20
child2.height = 20
child2.left = -10
child2.top = -10
child2.fill_color = aspose.pydrawing.Color.red
group.append_child(child2)
# أدرج مستطيلًا، ثم أدخل مستطيلًا أصغر قليلًا في نفس المكان مع صورة.
# الأشكال الأحدث التي نضيفها إلى المجموعة تتداخل مع الأشكال القديمة. سيتداخل المستطيل الأزرق الفاتح جزئيًا مع النجمة الحمراء،
# ثم سيتداخل الشكل الذي يحتوي على الصورة مع المستطيل الأزرق الفاتح، مستخدمًا إياه كإطار.
# لا يمكننا استخدام خصائص "ZOrder" للأشكال لتعديل ترتيبها داخل شكل مجموعة.
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
# أدرج مربع نص داخل شكل المجموعة. اضبط خاصية "Left" بحيث يكون الحافة اليمنى لمربع النص
# تلامس الحد الأيمن لحدود شكل المجموعة. اضبط خاصية "Top" بحيث يكون مربع النص خارجًا
# حدود شكل المجموعة، مع محاذاة حجمه العلوي على هامش أسفل شكل المجموعة.
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

