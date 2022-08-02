---
title: from_points method
second_title: Aspose.Words for Python via .NET API Reference
description: "A creation method that returns a new instance that represents a preferred width specified using a number of points."
type: docs
weight: 60
url: /python-net/aspose.words.tables/preferredwidth/from_points/
---

## from_points(points) {#float}

A creation method that returns a new instance that represents a preferred width specified using a number of points.


```python
def from_points(self, points: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| points | float |  |

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

Shows how to use unit conversion tools while specifying a preferred width for a cell.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_points(aw.ConvertUtil.inch_to_point(3))
builder.insert_cell()

self.assertEqual(216.0, table.first_row.first_cell.cell_format.preferred_width.value)
```

### See Also

* module [aspose.words.tables](../../)
* class [PreferredWidth](../)

