---
title: Table.clear_borders method
linktitle: clear_borders method
articleTitle: clear_borders method
second_title: Aspose.Words for Python
description: "Table.clear_borders method. Removes all table and cell borders on this table."
type: docs
weight: 370
url: /python-net/aspose.words.tables/table/clear_borders/
---

## clear_borders() {#default}

Removes all table and cell borders on this table.


```python
def clear_borders(self):
    ...
```

### Examples

Shows how to apply an outline border to a table.

```python
doc = aw.Document(MY_DIR + "Tables.docx")
table = doc.first_section.body.tables[0]

# Align the table to the center of the page.
table.alignment = aw.tables.TableAlignment.CENTER

# Clear any existing borders and shading from the table.
table.clear_borders()
table.clear_shading()

# Add green borders to the outline of the table.
table.set_border(aw.BorderType.LEFT, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)
table.set_border(aw.BorderType.RIGHT, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)
table.set_border(aw.BorderType.TOP, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)
table.set_border(aw.BorderType.BOTTOM, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)

# Fill the cells with a light green solid color.
table.set_shading(aw.TextureIndex.TEXTURE_SOLID, drawing.Color.light_green, drawing.Color.empty())

doc.save(ARTIFACTS_DIR + "Table.set_outline_borders.docx")
```

Shows how to remove all borders from a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("Hello world!")
builder.end_table()

# Modify the color and thickness of the top border.
top_border = table.first_row.row_format.borders.top
table.set_border(aw.BorderType.TOP, aw.LineStyle.DOUBLE, 1.5, drawing.Color.red, True)

self.assertEqual(1.5, top_border.line_width)
self.assertEqual(drawing.Color.red.to_argb(), top_border.color.to_argb())
self.assertEqual(aw.LineStyle.DOUBLE, top_border.line_style)

# Clear the borders of all cells in the table, and then save the document.
table.clear_borders()
doc.save(ARTIFACTS_DIR + "Table.borders.docx")

# Verify the values of the table's properties after re-opening the document.
doc = aw.Document(ARTIFACTS_DIR + "Table.borders.docx")
table = doc.first_section.body.tables[0]
top_border = table.first_row.row_format.borders.top

self.assertEqual(0.0, top_border.line_width)
self.assertEqual(drawing.Color.empty().to_argb(), top_border.color.to_argb())
self.assertEqual(aw.LineStyle.NONE, top_border.line_style)
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

