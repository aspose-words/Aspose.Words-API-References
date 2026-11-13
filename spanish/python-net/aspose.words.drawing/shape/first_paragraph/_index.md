---
title: Shape.first_paragraph property
linktitle: first_paragraph property
articleTitle: first_paragraph property
second_title: Aspose.Words for Python
description: "Shape.first_paragraph property. Gets the first paragraph in the shape."
type: docs
weight: 70
url: /es/python-net/aspose.words.drawing/shape/first_paragraph/
---

## Shape.first_paragraph property

Gets the first paragraph in the shape.


```python
@property
def first_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to create and format a text box.

```python
doc = aw.Document()
# Crea un cuadro de texto flotante.
text_box = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
text_box.wrap_type = aw.drawing.WrapType.NONE
text_box.height = 50
text_box.width = 200
# Establece la alineación horizontal y vertical del texto dentro de la forma.
text_box.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
text_box.vertical_alignment = aw.drawing.VerticalAlignment.TOP
# Añade un párrafo al cuadro de texto y agrega una ejecución de texto que el cuadro de texto mostrará.
text_box.append_child(aw.Paragraph(doc))
para = text_box.first_paragraph
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
run = aw.Run(doc=doc)
run.text = 'Hello world!'
para.append_child(run)
doc.first_section.body.first_paragraph.append_child(text_box)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.CreateTextBox.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

