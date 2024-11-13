---
title: TextBox.internal_margin_top property
linktitle: internal_margin_top property
articleTitle: internal_margin_top property
second_title: Aspose.Words for Python
description: "TextBox.internal_margin_top property. Specifies the inner top margin in points for a shape."
type: docs
weight: 50
url: /python-net/aspose.words.drawing/textbox/internal_margin_top/
---

## TextBox.internal_margin_top property

Specifies the inner top margin in points for a shape.


```python
@property
def internal_margin_top(self) -> float:
    ...

@internal_margin_top.setter
def internal_margin_top(self, value: float):
    ...

```

### Remarks

The default value is 1/20 inch.




### Examples

Shows how to set internal margins for a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert another textbox with specific margins.
text_box_shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=100, height=100)
text_box = text_box_shape.text_box
text_box.internal_margin_top = 15
text_box.internal_margin_bottom = 15
text_box.internal_margin_left = 15
text_box.internal_margin_right = 15
builder.move_to(text_box_shape.last_paragraph)
builder.write('Text placed according to textbox margins.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextBoxMargins.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

