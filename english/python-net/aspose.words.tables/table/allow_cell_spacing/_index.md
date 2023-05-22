---
title: Table.allow_cell_spacing property
linktitle: allow_cell_spacing property
articleTitle: allow_cell_spacing property
second_title: Aspose.Words for Python
description: "Table.allow_cell_spacing property. Gets or sets the Allow spacing between cells option."
type: docs
weight: 60
url: /python-net/aspose.words.tables/table/allow_cell_spacing/
---

## Table.allow_cell_spacing property

Gets or sets the "Allow spacing between cells" option.


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

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

