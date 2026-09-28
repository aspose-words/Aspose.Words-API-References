---
title: ShapeBase.bounds_in_points property
linktitle: bounds_in_points property
articleTitle: bounds_in_points property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_in_points property. Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape."
type: docs
weight: 80
url: /ar/python-net/aspose.words.drawing/shapebase/bounds_in_points/
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

