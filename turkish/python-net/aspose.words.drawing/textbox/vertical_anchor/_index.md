---
title: TextBox.vertical_anchor property
linktitle: vertical_anchor property
articleTitle: vertical_anchor property
second_title: Aspose.Words for Python
description: "TextBox.vertical_anchor property. Specifies the vertical alignment of the text within a shape."
type: docs
weight: 120
url: /tr/python-net/aspose.words.drawing/textbox/vertical_anchor/
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
# \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Top\" olarak ayarlayarak
# bu metin kutusundaki metni şeklin üst kenarıyla hizalayın.
# \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Middle\" olarak ayarlayarak
# bu metin kutusundaki metni şeklin ortasına hizalayın.
# "VerticalAnchor" özelliğini "TextBoxAnchor.Bottom" olarak ayarlayın
# metni bu metin kutusunda şeklin alt kısmına hizalayın.
shape.text_box.vertical_anchor = vertical_anchor
builder.move_to(shape.first_paragraph)
builder.write('Hello world!')
# Metin kutularındaki metnin dikey hizalanması Microsoft Word 2007 ve sonrasında kullanılabilir.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2007)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.VerticalAnchor.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

