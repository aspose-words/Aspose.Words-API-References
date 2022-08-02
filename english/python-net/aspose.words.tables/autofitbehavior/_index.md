---
title: AutoFitBehavior enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Determines how Aspose.Words resizes the table when you invoke the [Table.auto_fit()](../table/auto_fit/#autofitbehavior) method."
type: docs
weight: 10
url: /python-net/aspose.words.tables/autofitbehavior/
---

## AutoFitBehavior enumeration

Determines how Aspose.Words resizes the table when you invoke the [Table.auto_fit()](../table/auto_fit/#autofitbehavior) method.



### Members

| Name | Description |
| --- | --- |
| AUTO_FIT_TO_CONTENTS | Aspose.Words enables the AutoFit option, removes the preferred width from the table and all cells and then updates the table layout. |
| AUTO_FIT_TO_WINDOW | When you use this value, Aspose.Words enables the AutoFit option, sets the preferred width for the table to 100%,  removes preferred widths from all cells and then updates the table layout. |
| FIXED_COLUMN_WIDTHS | Aspose.Words disables the AutoFit option and removes the preferred with from the table. |

### Examples

Shows how to build a new table while applying a style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
table = builder.start_table()

# We must insert at least one row before setting any table formatting.
builder.insert_cell()

# Set the table style used based on the style identifier.
# Note that not all table styles are available when saving to .doc format.
table.style_identifier = aw.StyleIdentifier.MEDIUM_SHADING1_ACCENT1

# Partially apply the style to features of the table based on predicates, then build the table.
table.style_options = aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS | aw.tables.TableStyleOptions.FIRST_ROW
table.auto_fit(aw.tables.AutoFitBehavior.AUTO_FIT_TO_CONTENTS)

builder.writeln("Item")
builder.cell_format.right_padding = 40
builder.insert_cell()
builder.writeln("Quantity (kg)")
builder.end_row()

builder.insert_cell()
builder.writeln("Apples")
builder.insert_cell()
builder.writeln("20")
builder.end_row()

builder.insert_cell()
builder.writeln("Bananas")
builder.insert_cell()
builder.writeln("40")
builder.end_row()

builder.insert_cell()
builder.writeln("Carrots")
builder.insert_cell()
builder.writeln("50")
builder.end_row()

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_table_with_style.docx")
```

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

* module [aspose.words.tables](../)

