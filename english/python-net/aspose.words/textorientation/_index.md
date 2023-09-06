---
title: TextOrientation enumeration
linktitle: TextOrientation enumeration
articleTitle: TextOrientation enumeration
second_title: Aspose.Words for Python
description: "aspose.words.TextOrientation enumeration. Specifies orientation of text on a page, in a table cell or a text frame."
type: docs
weight: 1260
url: /python-net/aspose.words/textorientation/
---

## TextOrientation enumeration

Specifies orientation of text on a page, in a table cell or a text frame.


### Members

| Name | Description |
| --- | --- |
| HORIZONTAL | Text is arranged horizontally (lr-tb). |
| DOWNWARD | Text is rotated 90 degrees to the right to appear from top to bottom (tb-rl). |
| UPWARD | Text is rotated 90 degrees to the left to appear from bottom to top (bt-lr). |
| HORIZONTAL_ROTATED_FAR_EAST | Text is arranged horizontally, but Far East characters are rotated 90 degrees to the left (lr-tb-v). |
| VERTICAL_FAR_EAST | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom (tb-rl-v). |
| VERTICAL_ROTATED_FAR_EAST | Far East characters appear vertical, other text is rotated 90 degrees to the right to appear from top to bottom vertically, then left to right horizontally  (tb-lr-v). |

### Examples

Shows how to build a formatted 2x2 table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.write("Row 1, cell 1.")
builder.insert_cell()
builder.write("Row 1, cell 2.")
builder.end_row()

# While building the table, the document builder will apply its current row_format/cell_format property values
# to the current row/cell that its cursor is in and any new rows/cells as it creates them.
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[0].cell_format.vertical_alignment)
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[1].cell_format.vertical_alignment)

builder.insert_cell()
builder.row_format.height = 100
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write("Row 2, cell 1.")
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write("Row 2, cell 2.")
builder.end_row()
builder.end_table()

# Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
self.assertEqual(aw.TextOrientation.UPWARD, table.rows[1].cells[0].cell_format.orientation)
self.assertEqual(aw.TextOrientation.DOWNWARD, table.rows[1].cells[1].cell_format.orientation)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.build_table.docx")
```

### See Also

* module [aspose.words](../)

