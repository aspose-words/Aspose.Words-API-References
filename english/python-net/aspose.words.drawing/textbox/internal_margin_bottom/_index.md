﻿---
title: internal_margin_bottom property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the inner bottom margin in points for a shape."
type: docs
weight: 20
url: /python-net/aspose.words.drawing/textbox/internal_margin_bottom/
---

## TextBox.internal_margin_bottom property

Specifies the inner bottom margin in points for a shape.

The default value is 1/20 inch.




### Examples

Shows how to set internal margins for a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert another textbox with specific margins.
text_box_shape = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 100, 100)
text_box = text_box_shape.text_box
text_box.internal_margin_top = 15
text_box.internal_margin_bottom = 15
text_box.internal_margin_left = 15
text_box.internal_margin_right = 15

builder.move_to(text_box_shape.last_paragraph)
builder.write("Text placed according to textbox margins.")

doc.save(ARTIFACTS_DIR + "Shape.text_box_margins.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)
