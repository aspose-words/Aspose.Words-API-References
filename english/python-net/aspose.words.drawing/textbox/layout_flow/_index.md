---
title: TextBox.layout_flow property
linktitle: layout_flow property
articleTitle: layout_flow property
second_title: Aspose.Words for Python
description: "TextBox.layout_flow property. Determines the flow of the text layout in a shape."
type: docs
weight: 60
url: /python-net/aspose.words.drawing/textbox/layout_flow/
---

## TextBox.layout_flow property

Determines the flow of the text layout in a shape.

The default value is [LayoutFlow.HORIZONTAL](../../layoutflow/#HORIZONTAL).




### Examples

Shows how to set the orientation of text inside a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

text_box_shape = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 150, 100)
text_box = text_box_shape.text_box

# Move the document builder to inside the TextBox and add text.
builder.move_to(text_box_shape.last_paragraph)
builder.writeln("Hello world!")
builder.write("Hello again!")

# Set the "layout_flow" property to set an orientation for the text contents of this text box.
text_box.layout_flow = layout_flow

doc.save(ARTIFACTS_DIR + "Shape.text_box_layout_flow.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

