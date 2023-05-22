---
title: Cell.cell_format property
linktitle: cell_format property
articleTitle: cell_format property
second_title: Aspose.Words for Python
description: "Cell.cell_format property. Provides access to the formatting properties of the cell."
type: docs
weight: 20
url: /python-net/aspose.words.tables/cell/cell_format/
---

## Cell.cell_format property

Provides access to the formatting properties of the cell.


### Examples

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

Shows how to combine the rows from two tables into one.

```python
doc = aw.Document(MY_DIR + "Tables.docx")

# Below are two ways of getting a table from a document.
# 1 -  From the "tables" collection of a Body node:
first_table = doc.first_section.body.tables[0]

# 2 -  Using the "get_child" method:
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()

# Append all rows from the current table to the next.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)

# Remove the empty table container.
second_table.remove()

doc.save(ARTIFACTS_DIR + "Table.combine_tables.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

