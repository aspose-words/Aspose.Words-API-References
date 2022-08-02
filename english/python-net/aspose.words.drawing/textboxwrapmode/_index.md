---
title: TextBoxWrapMode enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies how text wraps inside a shape."
type: docs
weight: 390
url: /python-net/aspose.words.drawing/textboxwrapmode/
---

## TextBoxWrapMode enumeration

Specifies how text wraps inside a shape.


### Members

| Name | Description |
| --- | --- |
| SQUARE | Text wraps inside a shape. |
| NONE | Text does not wrap inside a shape. |

### Examples

Shows how to set a wrapping mode for the contents of a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

text_box_shape = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 300, 300)
text_box = text_box_shape.text_box

# Set the "text_box_wrap_mode" property to "TextBoxWrapMode.NONE" to increase the text box's width
# to accommodate text, should it be large enough.
# Set the "text_box_wrap_mode" property to "TextBoxWrapMode.SQUARE" to
# wrap all text inside the text box, preserving its dimensions.
text_box.text_box_wrap_mode = text_box_wrap_mode

builder.move_to(text_box_shape.last_paragraph)
builder.font.size = 32
builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")

doc.save(ARTIFACTS_DIR + "Shape.text_box_сontents_wrap_mode.docx")
```

### See Also

* module [aspose.words.drawing](../)

