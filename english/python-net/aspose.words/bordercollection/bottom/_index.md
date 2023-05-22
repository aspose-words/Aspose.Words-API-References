---
title: BorderCollection.bottom property
linktitle: bottom property
articleTitle: bottom property
second_title: Aspose.Words for Python
description: "BorderCollection.bottom property. Gets the bottom border."
type: docs
weight: 20
url: /python-net/aspose.words/bordercollection/bottom/
---

## BorderCollection.bottom property

Gets the bottom border.


### Examples

Shows how to apply border and shading color while building a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Start a table and set a default color/thickness for its borders.
table = builder.start_table()
table.set_borders(aw.LineStyle.SINGLE, 2.0, drawing.Color.black)

# Create a row with two cells with different background colors.
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = drawing.Color.light_sky_blue
builder.writeln("Row 1, Cell 1.")
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = drawing.Color.orange
builder.writeln("Row 1, Cell 2.")
builder.end_row()

# Reset cell formatting to disable the background colors
# set a custom border thickness for all new cells created by the builder,
# then build a second row.
builder.cell_format.clear_formatting()
builder.cell_format.borders.left.line_width = 4.0
builder.cell_format.borders.right.line_width = 4.0
builder.cell_format.borders.top.line_width = 4.0
builder.cell_format.borders.bottom.line_width = 4.0

builder.insert_cell()
builder.writeln("Row 2, Cell 1.")
builder.insert_cell()
builder.writeln("Row 2, Cell 2.")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.table_borders_and_shading.docx")
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

