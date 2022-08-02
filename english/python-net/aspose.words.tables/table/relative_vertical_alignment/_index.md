---
title: relative_vertical_alignment property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets floating table relative vertical alignment."
type: docs
weight: 240
url: /python-net/aspose.words.tables/table/relative_vertical_alignment/
---

## Table.relative_vertical_alignment property

Gets or sets floating table relative vertical alignment.


### Examples

Shows how set the location of floating tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.write("Table 1, cell 1")
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)

# Set the table's location to a place on the page, such as, in this case, the bottom right corner.
table.relative_vertical_alignment = aw.drawing.VerticalAlignment.BOTTOM
table.relative_horizontal_alignment = aw.drawing.HorizontalAlignment.RIGHT

table = builder.start_table()
builder.insert_cell()
builder.write("Table 2, cell 1")
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)

# We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
table.absolute_vertical_distance = 50
table.absolute_horizontal_distance = 100

doc.save(ARTIFACTS_DIR + "Table.change_floating_table_properties.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

