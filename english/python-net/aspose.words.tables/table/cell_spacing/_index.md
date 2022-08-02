---
title: cell_spacing property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the amount of space (in points) between the cells."
type: docs
weight: 100
url: /python-net/aspose.words.tables/table/cell_spacing/
---

## Table.cell_spacing property

Gets or sets the amount of space (in points) between the cells.


### Examples

Shows how to enable spacing between individual cells in a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("Animal")
builder.insert_cell()
builder.write("Class")
builder.end_row()
builder.insert_cell()
builder.write("Dog")
builder.insert_cell()
builder.write("Mammal")
builder.end_table()

table.cell_spacing = 3

# Set the "allow_cell_spacing" property to "True" to enable spacing between cells
# with a magnitude equal to the value of the "cell_spacing" property, in points.
# Set the "allow_cell_spacing" property to "False" to disable cell spacing
# and ignore the value of the "cell_spacing" property.
table.allow_cell_spacing = allow_cell_spacing

doc.save(ARTIFACTS_DIR + "Table.allow_cell_spacing.html")

# Adjusting the "cell_spacing" property will automatically enable cell spacing.
table.cell_spacing = 5

self.assertTrue(table.allow_cell_spacing)
```

Shows how to create custom style settings for the table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("Name")
builder.insert_cell()
builder.write("مرحبًا")
builder.end_row()
builder.insert_cell()
builder.insert_cell()
builder.end_table()

table_style = doc.styles.add(aw.StyleType.TABLE, "MyTableStyle1").as_table_style()
table_style.allow_break_across_pages = True
table_style.bidi = True
table_style.cell_spacing = 5
table_style.bottom_padding = 20
table_style.left_padding = 5
table_style.right_padding = 10
table_style.top_padding = 20
table_style.shading.background_pattern_color = drawing.Color.antique_white
table_style.borders.color = drawing.Color.blue
table_style.borders.line_style = aw.LineStyle.DOT_DASH
table_style.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER

table.style = table_style

# Setting the style properties of a table may affect the properties of the table itself.
self.assertTrue(table.bidi)
self.assertEqual(5.0, table.cell_spacing)
self.assertEqual("MyTableStyle1", table.style_name)

doc.save(ARTIFACTS_DIR + "Table.table_style_creation.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

