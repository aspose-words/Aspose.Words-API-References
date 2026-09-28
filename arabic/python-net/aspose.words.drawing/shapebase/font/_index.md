---
title: ShapeBase.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ShapeBase.font property. Provides access to the font formatting of this object."
type: docs
weight: 190
url: /ar/python-net/aspose.words.drawing/shapebase/font/
---

## ShapeBase.font property

Provides access to the font formatting of this object.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Examples

Shows how to insert a text box, and set the font of its contents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=300, height=50)
builder.move_to(shape.last_paragraph)
builder.write('This text is inside the text box.')
# اضبط خاصية "Hidden" لكائن "Font" الخاص بالشكل إلى "true" لإخفاء مربع النص عن الأنظار
# واستغنِ عن المساحة التي كان سيشغلها عادةً.
# اضبط خاصية "Hidden" لكائن "Font" الخاص بالشكل إلى "false" لجعل مربع النص مرئيًا.
shape.font.hidden = hide_shape
# إذا كان الشكل مرئيًا، سنقوم بتعديل مظهره عبر كائن الخط.
if not hide_shape:
    shape.font.highlight_color = aspose.pydrawing.Color.light_gray
    shape.font.color = aspose.pydrawing.Color.red
    shape.font.underline = aw.Underline.DASH
# انقل المُنشئ خارج مربع النص عائدًا إلى المستند الرئيسي.
builder.move_to(shape.parent_paragraph)
builder.writeln('\nThis text is outside the text box.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Font.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

