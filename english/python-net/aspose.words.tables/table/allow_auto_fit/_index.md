---
title: allow_auto_fit property
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents."
type: docs
weight: 50
url: /python-net/aspose.words.tables/table/allow_auto_fit/
---

## Table.allow_auto_fit property

Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.

The default value is ``True``.




### Examples

Shows how to enable/disable automatic table cell resizing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

table = builder.start_table()
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_points(100)
builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")

builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.AUTO
builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")
builder.end_row()
builder.end_table()

# Set the "allow_auto_fit" property to "False" to get the table to maintain the dimensions
# of all its rows and cells, and truncate contents if they get too large to fit.
# Set the "allow_auto_fit" property to "True" to allow the table to change its cells' width and height
# to accommodate their contents.
table.allow_auto_fit = allow_auto_fit

doc.save(ARTIFACTS_DIR + "Table.allow_auto_fit_on_table.html")
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)
* method [Table.auto_fit()](../auto_fit/#autofitbehavior)

