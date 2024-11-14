---
title: TextBox.fit_shape_to_text property
linktitle: fit_shape_to_text property
articleTitle: fit_shape_to_text property
second_title: Aspose.Words for Python
description: "TextBox.fit_shape_to_text property. Determines whether Microsoft Word will grow the shape to fit text."
type: docs
weight: 10
url: /python-net/aspose.words.drawing/textbox/fit_shape_to_text/
---

## TextBox.fit_shape_to_text property

Determines whether Microsoft Word will grow the shape to fit text.


```python
@property
def fit_shape_to_text(self) -> bool:
    ...

@fit_shape_to_text.setter
def fit_shape_to_text(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.




### Examples

Shows how to get a text box to resize itself to fit its contents tightly.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
text_box_shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=150, height=100)
text_box = text_box_shape.text_box
# Apply these values to both these members to get the parent shape to fit
# tightly around the text contents, ignoring the dimensions we have set.
text_box.fit_shape_to_text = True
text_box.text_box_wrap_mode = aw.drawing.TextBoxWrapMode.NONE
builder.move_to(text_box_shape.last_paragraph)
builder.write('Text fit tightly inside textbox.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextBoxFitShapeToText.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

