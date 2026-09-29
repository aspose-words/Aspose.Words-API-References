---
title: ShapeBase.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ShapeBase.font property. Provides access to the font formatting of this object."
type: docs
weight: 190
url: /it/python-net/aspose.words.drawing/shapebase/font/
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
# Imposta la proprietà "Hidden" dell'oggetto "Font" della forma su "true" per nascondere la casella di testo dalla vista
# e comprimere lo spazio che normalmente occuperebbe.
# Imposta la proprietà "Hidden" dell'oggetto "Font" della forma su "false" per lasciare la casella di testo visibile.
shape.font.hidden = hide_shape
# Se la forma è visibile, modificheremo il suo aspetto tramite l'oggetto font.
if not hide_shape:
    shape.font.highlight_color = aspose.pydrawing.Color.light_gray
    shape.font.color = aspose.pydrawing.Color.red
    shape.font.underline = aw.Underline.DASH
# Sposta il costruttore fuori dalla casella di testo e riportalo nel documento principale.
builder.move_to(shape.parent_paragraph)
builder.writeln('\nThis text is outside the text box.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Font.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

