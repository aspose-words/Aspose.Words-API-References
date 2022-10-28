---
title: paragraph_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns an object that represents current paragraph formatting properties."
type: docs
weight: 170
url: /python-net/aspose.words/documentbuilder/paragraph_format/
---

## DocumentBuilder.paragraph_format property

Returns an object that represents current paragraph formatting properties.


### Examples

Shows how to create a formatted table using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
table.left_indent = 20

# Set some formatting options for text and table appearance.
builder.row_format.height = 40
builder.row_format.height_rule = aw.HeightRule.AT_LEAST
builder.cell_format.shading.background_pattern_color = drawing.Color.from_argb(198, 217, 241)

builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.font.size = 16
builder.font.name = "Arial"
builder.font.bold = True

# Configuring the formatting options in a document builder will apply them
# to the current cell/row its cursor is in,
# as well as any new cells and rows created using that builder.
builder.write("Header Row,\n Cell 1")
builder.insert_cell()
builder.write("Header Row,\n Cell 2")
builder.insert_cell()
builder.write("Header Row,\n Cell 3")
builder.end_row()

# Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
# The builder will not apply these to the first row already created so that it will stand out as a header row.
builder.cell_format.shading.background_pattern_color = drawing.Color.white
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.row_format.height = 30
builder.row_format.height_rule = aw.HeightRule.AUTO
builder.insert_cell()
builder.font.size = 12
builder.font.bold = False

builder.write("Row 1, Cell 1.")
builder.insert_cell()
builder.write("Row 1, Cell 2.")
builder.insert_cell()
builder.write("Row 1, Cell 3.")
builder.end_row()
builder.insert_cell()
builder.write("Row 2, Cell 1.")
builder.insert_cell()
builder.write("Row 2, Cell 2.")
builder.insert_cell()
builder.write("Row 2, Cell 3.")
builder.end_row()
builder.end_table()

doc.save(ARTIFACTS_DIR + "DocumentBuilder.build_formatted_table.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

