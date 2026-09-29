---
title: TextBoxAnchor enumeration
linktitle: TextBoxAnchor enumeration
articleTitle: TextBoxAnchor enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.TextBoxAnchor enumeration. Specifies values used for shape text vertical alignment."
type: docs
weight: 460
url: /es/python-net/aspose.words.drawing/textboxanchor/
---

## TextBoxAnchor enumeration

Specifies values used for shape text vertical alignment.


### Members

| Name | Description |
| --- | --- |
| TOP | Text is aligned to the top of the textbox. |
| MIDDLE | Text is aligned to the middle of the textbox. |
| BOTTOM | Text is aligned to the bottom of the textbox. |
| TOP_CENTERED | Text is aligned to the top centered of the textbox. |
| MIDDLE_CENTERED | Text is aligned to the middle centered of the textbox. |
| BOTTOM_CENTERED | Text is aligned to the bottom centered of the textbox. |
| TOP_BASELINE | Text is aligned to the top baseline of the textbox. |
| BOTTOM_BASELINE | Text is aligned to the bottom baseline of the textbox. |
| TOP_CENTERED_BASELINE | Text is aligned to the top centered baseline of the textbox. |
| BOTTOM_CENTERED_BASELINE | Text is aligned to the bottom centered baseline of the textbox. |

### Examples

Shows how to vertically align the text contents of a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=200, height=200)
# Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Top" para
# alinear el texto en este cuadro de texto con el lado superior de la forma.
# Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Middle" para
# alinear el texto en este cuadro de texto al centro de la forma.
# Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Bottom" para
# alinear el texto en este cuadro de texto al borde inferior de la forma.
shape.text_box.vertical_anchor = vertical_anchor
builder.move_to(shape.first_paragraph)
builder.write('Hello world!')
# La alineación vertical del texto dentro de los cuadros de texto está disponible a partir de Microsoft Word 2007.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2007)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.VerticalAnchor.docx')
```

### See Also

* module [aspose.words.drawing](../)

