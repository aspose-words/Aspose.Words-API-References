---
title: ShapeBase.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ShapeBase.font property. Provides access to the font formatting of this object."
type: docs
weight: 190
url: /sv/python-net/aspose.words.drawing/shapebase/font/
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
# Ställ in egenskapen \"Hidden\" för formens \"Font\"-objekt till \"true\" för att dölja textrutan från synen
# och kollapsa det utrymme den normalt skulle uppta.
# Ställ in egenskapen \"Hidden\" för formens \"Font\"-objekt till \"false\" för att låta textrutan vara synlig.
shape.font.hidden = hide_shape
# Om formen är synlig kommer vi att ändra dess utseende via teckenobjektet.
if not hide_shape:
    shape.font.highlight_color = aspose.pydrawing.Color.light_gray
    shape.font.color = aspose.pydrawing.Color.red
    shape.font.underline = aw.Underline.DASH
# Flytta byggaren från textrutan tillbaka till huvuddokumentet.
builder.move_to(shape.parent_paragraph)
builder.writeln('\nThis text is outside the text box.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Font.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

