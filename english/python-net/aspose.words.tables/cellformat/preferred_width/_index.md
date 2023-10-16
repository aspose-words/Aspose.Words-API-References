---
title: CellFormat.preferred_width property
linktitle: preferred_width property
articleTitle: preferred_width property
second_title: Aspose.Words for Python
description: "CellFormat.preferred_width property. Returns or sets the preferred width of the cell."
type: docs
weight: 80
url: /python-net/aspose.words.tables/cellformat/preferred_width/
---

## CellFormat.preferred_width property

Returns or sets the preferred width of the cell.

The preferred width (along with the table's Auto Fit option) determines how the actual
width of the cell is calculated by the table layout algorithm. Table layout can be performed by
Aspose.Words when it saves the document or by Microsoft Word when it displays the document.

The preferred width can be specified in points or in percent. The preferred width
can also be specified as "auto", which means no preferred width is specified.

The default value is [PreferredWidth.AUTO](../../preferredwidth/AUTO/).




### Examples

Shows how to set a preferred width for table cells.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
table = builder.start_table()

# There are two ways of applying the "PreferredWidth" class to table cells.
# 1 -  Set an absolute preferred width based on points:
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_points(40)
builder.cell_format.shading.background_pattern_color = drawing.Color.light_yellow
builder.writeln(f"Cell with a width of {builder.cell_format.preferred_width}.")

# 2 -  Set a relative preferred width based on percent of the table's width:
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_percent(20)
builder.cell_format.shading.background_pattern_color = drawing.Color.light_blue
builder.writeln(f"Cell with a width of {builder.cell_format.preferred_width}.")

builder.insert_cell()

# A cell with no preferred width specified will take up the rest of the available space.
builder.cell_format.preferred_width = aw.tables.PreferredWidth.AUTO

# Each configuration of the "preferred_width" property creates a new object.
self.assertTrue(table.first_row.cells[1].cell_format.preferred_width is not builder.cell_format.preferred_width)

builder.cell_format.shading.background_pattern_color = drawing.Color.light_green
builder.writeln("Automatically sized cell.")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_cells_with_preferred_widths.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)
* property [CellFormat.width](../width/)

