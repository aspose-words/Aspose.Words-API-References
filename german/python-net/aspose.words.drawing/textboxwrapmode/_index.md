---
title: TextBoxWrapMode enumeration
linktitle: TextBoxWrapMode enumeration
articleTitle: TextBoxWrapMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.TextBoxWrapMode enumeration. Specifies how text wraps inside a shape."
type: docs
weight: 470
url: /de/python-net/aspose.words.drawing/textboxwrapmode/
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
builder = aw.DocumentBuilder(doc=doc)
text_box_shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=300, height=300)
text_box = text_box_shape.text_box
# Setzen Sie die "TextBoxWrapMode"-Eigenschaft auf "TextBoxWrapMode.None", um die Breite des Textfelds zu erhöhen
# um Text aufzunehmen, falls er groß genug ist.
# Setzen Sie die "TextBoxWrapMode"-Eigenschaft auf "TextBoxWrapMode.Square", um
# den gesamten Text im Textfeld zu umbrechen und dabei seine Abmessungen beizubehalten.
text_box.text_box_wrap_mode = text_box_wrap_mode
builder.move_to(text_box_shape.last_paragraph)
builder.font.size = 32
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextBoxContentsWrapMode.docx')
```

### See Also

* module [aspose.words.drawing](../)

