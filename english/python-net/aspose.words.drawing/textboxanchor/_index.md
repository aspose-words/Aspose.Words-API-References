---
title: TextBoxAnchor enumeration
linktitle: TextBoxAnchor enumeration
articleTitle: TextBoxAnchor enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.TextBoxAnchor enumeration. Specifies values used for shape text vertical alignment."
type: docs
weight: 460
url: /python-net/aspose.words.drawing/textboxanchor/
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

* module [aspose.words.drawing](../)

