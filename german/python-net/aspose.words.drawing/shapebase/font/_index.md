---
title: ShapeBase.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ShapeBase.font property. Provides access to the font formatting of this object."
type: docs
weight: 190
url: /de/python-net/aspose.words.drawing/shapebase/font/
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
# Setzen Sie die "Hidden"-Eigenschaft des "Font"-Objekts der Form auf "true", um das Textfeld zu verbergen
# und reduzieren Sie den Raum, den es normalerweise einnehmen würde.
# Setzen Sie die "Hidden"-Eigenschaft des "Font"-Objekts der Form auf "false", um das Textfeld sichtbar zu lassen.
shape.font.hidden = hide_shape
# Wenn die Form sichtbar ist, werden wir ihr Aussehen über das Font-Objekt ändern.
if not hide_shape:
    shape.font.highlight_color = aspose.pydrawing.Color.light_gray
    shape.font.color = aspose.pydrawing.Color.red
    shape.font.underline = aw.Underline.DASH
# Verschieben Sie den Builder aus dem Textfeld zurück in das Hauptdokument.
builder.move_to(shape.parent_paragraph)
builder.writeln('\nThis text is outside the text box.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Font.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

