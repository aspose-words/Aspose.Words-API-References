---
title: TextBox.internal_margin_left property
linktitle: internal_margin_left property
articleTitle: internal_margin_left property
second_title: Aspose.Words for Python
description: "TextBox.internal_margin_left property. Specifies the inner left margin in points for a shape."
type: docs
weight: 30
url: /python-net/aspose.words.drawing/textbox/internal_margin_left/
---

## TextBox.internal_margin_left property

Specifies the inner left margin in points for a shape.


```python
@property
def internal_margin_left(self) -> float:
    ...

@internal_margin_left.setter
def internal_margin_left(self, value: float):
    ...

```

### Remarks

The default value is 1/10 inch.




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

