﻿---
title: Shape.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Shape.last_paragraph property. Gets the last paragraph in the shape."
type: docs
weight: 130
url: /python-net/aspose.words.drawing/shape/last_paragraph/
---

## Shape.last_paragraph property

Gets the last paragraph in the shape.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to set the orientation of text inside a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
text_box_shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=150, height=100)
text_box = text_box_shape.text_box
# Move the document builder to inside the TextBox and add text.
builder.move_to(text_box_shape.last_paragraph)
builder.writeln('Hello world!')
builder.write('Hello again!')
# Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
text_box.layout_flow = layout_flow
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextBoxLayoutFlow.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

