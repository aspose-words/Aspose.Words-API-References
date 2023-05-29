---
title: PreferredWidth.from_percent method
linktitle: from_percent method
articleTitle: from_percent method
second_title: Aspose.Words for Python
description: "PreferredWidth.from_percent method. A creation method that returns a new instance that represents a preferred width specified as a percentage."
type: docs
weight: 50
url: /python-net/aspose.words.tables/preferredwidth/from_percent/
---

## from_percent(percent) {#float}

A creation method that returns a new instance that represents a preferred width specified as a percentage.


```python
def from_percent(self, percent: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| percent | float |  |

### Examples

Shows how to set a table to auto fit to 50% of the width of the page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("Cell #1")
builder.insert_cell()
builder.write("Cell #2")
builder.insert_cell()
builder.write("Cell #3")

table.preferred_width = aw.tables.PreferredWidth.from_percent(50)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_table_with_preferred_width.docx")
```

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
* class [PreferredWidth](../)

