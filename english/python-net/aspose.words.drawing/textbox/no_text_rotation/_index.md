﻿---
title: TextBox.no_text_rotation property
linktitle: no_text_rotation property
articleTitle: no_text_rotation property
second_title: Aspose.Words for Python
description: "TextBox.no_text_rotation property. Gets or sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated."
type: docs
weight: 80
url: /python-net/aspose.words.drawing/textbox/no_text_rotation/
---

## TextBox.no_text_rotation property

Gets or sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated.


```python
@property
def no_text_rotation(self) -> bool:
    ...

@no_text_rotation.setter
def no_text_rotation(self, value: bool):
    ...

```

### Remarks

The default value is ``False``





### Examples

Shows how to disable text rotation when the shape is rotate.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.ELLIPSE, width=20, height=20)
shape.text_box.no_text_rotation = True
doc.save(file_name=ARTIFACTS_DIR + 'Shape.NoTextRotation.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

