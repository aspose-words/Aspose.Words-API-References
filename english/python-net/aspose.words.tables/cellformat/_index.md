---
title: CellFormat class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents all formatting for a table cell"
type: docs
weight: 40
url: /python-net/aspose.words.tables/cellformat/
---

## CellFormat class

Represents all formatting for a table cell.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/python-net/working-with-tables/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [borders](./borders/) | Gets collection of borders of the cell. |
| [bottom_padding](./bottom_padding/) | Returns or sets the amount of space (in points) to add below the contents of cell. |
| [fit_text](./fit_text/) | If ``True``, fits text in the cell, compressing each paragraph to the width of the cell. |
| [horizontal_merge](./horizontal_merge/) | Specifies how the cell is merged horizontally with other cells in the row. |
| [left_padding](./left_padding/) | Returns or sets the amount of space (in points) to add to the left of the contents of cell. |
| [orientation](./orientation/) | Returns or sets the orientation of text in a table cell. |
| [preferred_width](./preferred_width/) | Returns or sets the preferred width of the cell. |
| [right_padding](./right_padding/) | Returns or sets the amount of space (in points) to add to the right of the contents of cell. |
| [shading](./shading/) | Returns a [Shading](../../aspose.words/shading/) object that refers to the shading formatting for the cell. |
| [top_padding](./top_padding/) | Returns or sets the amount of space (in points) to add above the contents of cell. |
| [vertical_alignment](./vertical_alignment/) | Returns or sets the vertical alignment of text in the cell. |
| [vertical_merge](./vertical_merge/) | Specifies how the cell is merged with other cells vertically. |
| [width](./width/) | Gets the width of the cell in points. |
| [wrap_text](./wrap_text/) | If ``True``, wrap text for the cell. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Resets to default cell formatting. Does not change the width of the cell. |
|[ set_paddings(left_padding, top_padding, right_padding, bottom_padding)](./set_paddings/#float_float_float_float) | Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell. |

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

Shows how to modify the format of rows and cells in a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("City")
builder.insert_cell()
builder.write("Country")
builder.end_row()
builder.insert_cell()
builder.write("London")
builder.insert_cell()
builder.write("U.K.")
builder.end_table()

# Use the first row's "row_format" property to modify the formatting
# of the contents of all cells in this row.
row_format = table.first_row.row_format
row_format.height = 25
row_format.borders.bottom.color = drawing.Color.red

# Use the "cell_format" property of the first cell in the last row to modify the formatting of that cell's contents.
cell_format = table.last_row.first_cell.cell_format
cell_format.width = 100
cell_format.shading.background_pattern_color = drawing.Color.orange

doc.save(ARTIFACTS_DIR + "Table.row_cell_format.docx")
```

Shows how to modify formatting of a table cell.

```python
doc = aw.Document(MY_DIR + "Tables.docx")
table = doc.first_section.body.tables[0]
first_cell = table.first_row.first_cell

# Use a cell's "cell_format" property to set formatting that modifies the appearance of that cell.
first_cell.cell_format.width = 30
first_cell.cell_format.orientation = aw.TextOrientation.DOWNWARD
first_cell.cell_format.shading.foreground_pattern_color = drawing.Color.light_green

doc.save(ARTIFACTS_DIR + "Table.cell_format.docx")
```

### See Also

* module [aspose.words.tables](../)

