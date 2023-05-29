---
title: LayoutFlow enumeration
linktitle: LayoutFlow enumeration
articleTitle: LayoutFlow enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.LayoutFlow enumeration. Determines the flow of the text layout in a textbox."
type: docs
weight: 210
url: /python-net/aspose.words.drawing/layoutflow/
---

## LayoutFlow enumeration

Determines the flow of the text layout in a textbox.


### Members

| Name | Description |
| --- | --- |
| HORIZONTAL | Text is displayed horizontally. |
| TOP_TO_BOTTOM_IDEOGRAPHIC | Ideographic text is displayed vertically. |
| BOTTOM_TO_TOP | Text is displayed vertically. |
| TOP_TO_BOTTOM | Text is displayed vertically. |
| HORIZONTAL_IDEOGRAPHIC | Ideographic text is displayed horizontally. |
| VERTICAL | Text is displayed vertically. |

### Examples

Shows how to add text to a text box, and change its orientation

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

textbox = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
textbox.width = 100
textbox.height = 100
textbox.text_box.layout_flow = aw.drawing.LayoutFlow.BOTTOM_TO_TOP

textbox.append_child(aw.Paragraph(doc))
builder.insert_node(textbox)

builder.move_to(textbox.first_paragraph)
builder.write("This text is flipped 90 degrees to the left.")

doc.save(ARTIFACTS_DIR + "Drawing.text_box.docx")
```

### See Also

* module [aspose.words.drawing](../)
* property [TextBox.layout_flow](../textbox/layout_flow/)

