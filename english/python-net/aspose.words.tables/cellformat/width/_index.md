---
title: CellFormat.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for Python
description: "CellFormat.width property. Gets the width of the cell in points."
type: docs
weight: 140
url: /python-net/aspose.words.tables/cellformat/width/
---

## CellFormat.width property

Gets the width of the cell in points.

The width is calculated by Aspose.Words on document loading and saving.
Currently, not every combination of table, cell and document properties is supported.
The returned value may not be accurate for some documents.
It may not exactly match the cell width as calculated by MS Word when the document is opened in MS Word.

Setting this property is not recommended.
There is no guarantee that the cell will actually have the set width.
The width may be adjusted to accommodate cell contents in an auto-fit table layout.
Cells in other rows may have conflicting width settings.
The table may be resized to fit into the container or to meet table width settings.
Consider using [CellFormat.preferred_width](../preferred_width/) for setting the cell width.
Setting this property sets [CellFormat.preferred_width](../preferred_width/) implicitly since version 15.8.





### Examples

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.start_table()

# Setting table formatting options for a document builder
# will apply them to every row and cell that we add with it.
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER

builder.cell_format.clear_formatting()
builder.cell_format.width = 150
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.cell_format.shading.background_pattern_color = drawing.Color.green_yellow
builder.cell_format.wrap_text = False
builder.cell_format.fit_text = True

builder.row_format.clear_formatting()
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.row_format.height = 50
builder.row_format.borders.line_style = aw.LineStyle.ENGRAVE_3D
builder.row_format.borders.color = drawing.Color.orange

builder.insert_cell()
builder.write("Row 1, Col 1")

builder.insert_cell()
builder.write("Row 1, Col 2")
builder.end_row()

# Changing the formatting will apply it to the current cell,
# and any new cells that we create with the builder afterward.
# This will not affect the cells that we have added previously.
builder.cell_format.shading.clear_formatting()

builder.insert_cell()
builder.write("Row 2, Col 1")

builder.insert_cell()
builder.write("Row 2, Col 2")

builder.end_row()

# Increase row height to fit the vertical text.
builder.insert_cell()
builder.row_format.height = 150
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write("Row 3, Col 1")

builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write("Row 3, Col 2")

builder.end_row()
builder.end_table()

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_table.docx")
```

Shows how to format cells with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("Row 1, cell 1.")

# Insert a second cell, and then configure cell text padding options.
# The builder will apply these settings at its current cell, and any new cells creates afterwards.
builder.insert_cell()

cell_format = builder.cell_format
cell_format.width = 250
cell_format.left_padding = 30
cell_format.right_padding = 30
cell_format.top_padding = 30
cell_format.bottom_padding = 30

builder.write("Row 1, cell 2.")
builder.end_row()
builder.end_table()

# The first cell was unaffected by the padding reconfiguration, and still holds the default values.
self.assertEqual(0.0, table.first_row.cells[0].cell_format.width)
self.assertEqual(5.4, table.first_row.cells[0].cell_format.left_padding)
self.assertEqual(5.4, table.first_row.cells[0].cell_format.right_padding)
self.assertEqual(0.0, table.first_row.cells[0].cell_format.top_padding)
self.assertEqual(0.0, table.first_row.cells[0].cell_format.bottom_padding)

self.assertEqual(250.0, table.first_row.cells[1].cell_format.width)
self.assertEqual(30.0, table.first_row.cells[1].cell_format.left_padding)
self.assertEqual(30.0, table.first_row.cells[1].cell_format.right_padding)
self.assertEqual(30.0, table.first_row.cells[1].cell_format.top_padding)
self.assertEqual(30.0, table.first_row.cells[1].cell_format.bottom_padding)

# The first cell will still grow in the output document to match the size of its neighboring cell.
doc.save(ARTIFACTS_DIR + "DocumentBuilder.set_cell_formatting.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)
* property [CellFormat.preferred_width](../preferred_width/)

