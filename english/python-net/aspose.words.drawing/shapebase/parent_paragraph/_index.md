---
title: ShapeBase.parent_paragraph property
linktitle: parent_paragraph property
articleTitle: parent_paragraph property
second_title: Aspose.Words for Python
description: "ShapeBase.parent_paragraph property. Returns the immediate parent paragraph."
type: docs
weight: 410
url: /python-net/aspose.words.drawing/shapebase/parent_paragraph/
---

## ShapeBase.parent_paragraph property

Returns the immediate parent paragraph.


```python
@property
def parent_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Remarks

For child shapes of a group shape and child shapes of an Office Math object always returns ``None``.


### Examples

Shows how to insert a text box, and set the font of its contents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")

shape = builder.insert_shape(aw.drawing.ShapeType.TEXT_BOX, 300, 50)
builder.move_to(shape.last_paragraph)
builder.write("This text is inside the text box.")

# Set the "hidden" property of the shape's "font" object to "True" to hide the text box from sight
# and collapse the space that it would normally occupy.
# Set the "hidden" property of the shape's "font" object to "False" to leave the text box visible.
shape.font.hidden = hide_shape

# If the shape is visible, we will modify its appearance via the font object.
if not hide_shape:
    shape.font.highlight_color = drawing.Color.light_gray
    shape.font.color = drawing.Color.red
    shape.font.underline = aw.Underline.DASH

# Move the builder out of the text box back into the main document.
builder.move_to(shape.parent_paragraph)

builder.writeln("\nThis text is outside the text box.")

doc.save(ARTIFACTS_DIR + "Shape.font.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

