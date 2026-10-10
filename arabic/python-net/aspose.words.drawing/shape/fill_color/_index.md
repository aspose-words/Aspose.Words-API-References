---
title: Shape.fill_color property
linktitle: fill_color property
articleTitle: fill_color property
second_title: Aspose.Words for Python
description: "Shape.fill_color property. Defines the brush color that fills the closed path of the shape."
type: docs
weight: 50
url: /ar/python-net/aspose.words.drawing/shape/fill_color/
---

## Shape.fill_color property

Defines the brush color that fills the closed path of the shape.


```python
@property
def fill_color(self) -> aspose.pydrawing.Color:
    ...

@fill_color.setter
def fill_color(self, value: aspose.pydrawing.Color):
    ...

```

### Remarks

This is a shortcut to the [Fill.color](../../fill/color/) property.

The default value is
aspose.pydrawing.Color.white.





### Examples

Shows how to fill a shape with a solid color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# اكتب بعض النص، ثم غطه بشكل عائم.
builder.font.size = 32
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CLOUD_CALLOUT, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=25, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=25, width=250, height=150, wrap_type=aw.drawing.WrapType.NONE)
# استخدم خاصية "StrokeColor" لتعيين لون حدود الشكل.
shape.stroke_color = aspose.pydrawing.Color.cadet_blue
# استخدم خاصية "FillColor" لتعيين لون المنطقة الداخلية للشكل.
shape.fill_color = aspose.pydrawing.Color.light_blue
# خاصية "Opacity" تحدد مدى شفافية اللون على مقياس من 0 إلى 1،
# حيث 1 يعني غير شفاف تمامًا، و0 يعني غير مرئي.
# تعبئة الشكل بشكل افتراضي غير شفافة تمامًا، لذا لا يمكننا رؤية النص الذي يقع فوقه الشكل.
self.assertEqual(1, shape.fill.opacity)
# قم بتعيين شفافية لون تعبئة الشكل إلى قيمة أقل حتى نتمكن من رؤية النص تحته.
shape.fill.opacity = 0.3
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Fill.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

