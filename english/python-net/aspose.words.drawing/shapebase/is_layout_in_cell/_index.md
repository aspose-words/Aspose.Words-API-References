---
title: ShapeBase.is_layout_in_cell property
linktitle: is_layout_in_cell property
articleTitle: is_layout_in_cell property
second_title: Aspose.Words for Python
description: "ShapeBase.is_layout_in_cell property. Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it."
type: docs
weight: 320
url: /python-net/aspose.words.drawing/shapebase/is_layout_in_cell/
---

## ShapeBase.is_layout_in_cell property

Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it.


```python
@property
def is_layout_in_cell(self) -> bool:
    ...

@is_layout_in_cell.setter
def is_layout_in_cell(self, value: bool):
    ...

```

### Remarks

The default value is ``True``.

Has effect only for top level shapes, the property [ShapeBase.wrap_type](../wrap_type/) of which is set to value
other than [Inline](../../../aspose.words/inline/).




### Examples

Shows how to determine how to display a shape in a table cell.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.insert_cell()
builder.end_table()

table_style = doc.styles.add(aw.StyleType.TABLE, "MyTableStyle1").as_table_style()
table_style.bottom_padding = 20
table_style.left_padding = 10
table_style.right_padding = 10
table_style.top_padding = 20
table_style.borders.color = drawing.Color.black
table_style.borders.line_style = aw.LineStyle.SINGLE

table.style = table_style

builder.move_to(table.first_row.first_cell.first_paragraph)

shape = builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, 50,
    aw.drawing.RelativeVerticalPosition.TOP_MARGIN, 100, 100, 100, aw.drawing.WrapType.NONE)

# Set the "is_layout_in_cell" property to "True" to display the shape as an inline element inside the cell's paragraph.
# The coordinate origin that will determine the shape's location will be the top left corner of the shape's cell.
# If we re-size the cell, the shape will move to maintain the same position starting from the cell's top left.
# Set the "is_layout_in_cell" property to "False" to display the shape as an independent floating shape.
# The coordinate origin that will determine the shape's location will be the top left corner of the page,
# and the shape will not respond to any re-sizing of its cell.
shape.is_layout_in_cell = is_layout_in_cell

# We can only apply the "is_layout_in_cell" property to floating shapes.
shape.wrap_type = aw.drawing.WrapType.NONE

doc.save(ARTIFACTS_DIR + "Shape.is_layout_in_cell.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

