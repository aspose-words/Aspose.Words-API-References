---
title: ShapeBase.parent_paragraph property
linktitle: parent_paragraph property
articleTitle: parent_paragraph property
second_title: Aspose.Words for Python
description: "ShapeBase.parent_paragraph property. Returns the immediate parent paragraph."
type: docs
weight: 430
url: /es/python-net/aspose.words.drawing/shapebase/parent_paragraph/
---

## ShapeBase.parent_paragraph property

Returns the immediate parent paragraph.


```python
@property
def parent_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Remarks

For child shapes of a group shape and child shapes of an Office Math object always returns ``None``.


### Examples

Shows how to insert a text box, and set the font of its contents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=300, height=50)
builder.move_to(shape.last_paragraph)
builder.write('This text is inside the text box.')
# Establece la propiedad "Hidden" del objeto "Font" de la forma a "true" para ocultar el cuadro de texto de la vista
# y colapsa el espacio que normalmente ocuparía.
# Establece la propiedad "Hidden" del objeto "Font" de la forma a "false" para dejar el cuadro de texto visible.
shape.font.hidden = hide_shape
# Si la forma es visible, modificaremos su apariencia a través del objeto de fuente.
if not hide_shape:
    shape.font.highlight_color = aspose.pydrawing.Color.light_gray
    shape.font.color = aspose.pydrawing.Color.red
    shape.font.underline = aw.Underline.DASH
# Mueve el generador fuera del cuadro de texto de regreso al documento principal.
builder.move_to(shape.parent_paragraph)
builder.writeln('\nThis text is outside the text box.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Font.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

