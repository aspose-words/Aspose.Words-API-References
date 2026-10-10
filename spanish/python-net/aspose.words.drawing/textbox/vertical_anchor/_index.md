---
title: TextBox.vertical_anchor property
linktitle: vertical_anchor property
articleTitle: vertical_anchor property
second_title: Aspose.Words for Python
description: "TextBox.vertical_anchor property. Specifies the vertical alignment of the text within a shape."
type: docs
weight: 120
url: /es/python-net/aspose.words.drawing/textbox/vertical_anchor/
---

## TextBox.vertical_anchor property

Specifies the vertical alignment of the text within a shape.


```python
@property
def vertical_anchor(self) -> aspose.words.drawing.TextBoxAnchor:
    ...

@vertical_anchor.setter
def vertical_anchor(self, value: aspose.words.drawing.TextBoxAnchor):
    ...

```

### Remarks

The default value is [TextBoxAnchor.TOP](../../textboxanchor/#TOP).




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

* module [aspose.words.drawing](../../)
* class [TextBox](../)

