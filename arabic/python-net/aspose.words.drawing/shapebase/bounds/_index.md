---
title: ShapeBase.bounds property
linktitle: bounds property
articleTitle: bounds property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds property. Gets or sets the location and size of the containing block of the shape."
type: docs
weight: 70
url: /ar/python-net/aspose.words.drawing/shapebase/bounds/
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

Shows how to verify shape containing block boundaries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.LINE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=50, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=50, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.stroke_color = aspose.pydrawing.Color.orange
# على الرغم من أن الخط نفسه يشغل مساحة قليلة على صفحة المستند،
# إلا أنه يشغل كتلة مستطيلة حاوية، يمكننا تحديد حجمها باستخدام خصائص "Bounds".
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)
# أنشئ شكل مجموعة، ثم اضبط حجم كتلته الحاوية باستخدام خاصية "Bounds".
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(0, 100, 250, 250)
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
# أنشئ مستطيلًا، تحقق من حجم كتلته الحدودية، ثم أضفه إلى شكل المجموعة.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
self.assertEqual(aspose.pydrawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)
group.append_child(shape)
# مستوى إحداثيات شكل المجموعة له أصله في الزاوية العلوية اليسرى لكتلته الحاوية،
# والإحداثيات x و y هي (1000, 1000) في الزاوية السفلية اليمنى.
# شكل مجموعتنا حجمه 250×250 نقطة، لذا كل 4 نقاط على مستوى إحداثيات شكل المجموعة
# تُترجم إلى نقطة واحدة في مستوى إحداثيات جسم المستند.
# كل شكل نقوم بإدراجه سيتقلص أيضًا في الحجم بمعامل 4.
# سيعكس التغيير في خاصية "BoundsInPoints" للشكل ذلك.
self.assertEqual(aspose.pydrawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)
doc.first_section.body.first_paragraph.append_child(group)
# أدرج شكلاً وضعه خارج حدود كتلة الشكل المجموعة الحاوية.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000
group.append_child(shape)
# لقد زادت بصمة شكل المجموعة في جسم المستند، لكن الكتلة الحاوية تبقى كما هي.
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(aspose.pydrawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Bounds.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

