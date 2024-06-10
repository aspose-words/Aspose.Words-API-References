---
title: TextBox.vertical_anchor property
linktitle: vertical_anchor property
articleTitle: vertical_anchor property
second_title: Aspose.Words for Python
description: "TextBox.vertical_anchor property. Specifies the vertical alignment of the text within a shape."
type: docs
weight: 120
url: /python-net/aspose.words.drawing/textbox/vertical_anchor/
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
builder = aw.DocumentBuilder(doc)
shape = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 200, 200)
# Set the "vertical_anchor" property to "TextBoxAnchor.TOP" to
# align the text in this text box with the top side of the shape.
# Set the "vertical_anchor" property to "TextBoxAnchor.MIDDLE" to
# align the text in this text box to the center of the shape.
# Set the "vertical_anchor" property to "TextBoxAnchor.BOTTOM" to
# align the text in this text box to the bottom of the shape.
shape.text_box.vertical_anchor = vertical_anchor
builder.move_to(shape.first_paragraph)
builder.write('Hello world!')
# The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2007)
doc.save(ARTIFACTS_DIR + 'Shape.vertical_anchor.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

